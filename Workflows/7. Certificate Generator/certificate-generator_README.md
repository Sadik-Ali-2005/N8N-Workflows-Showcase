# **Certificate Generator (n8n)**

## **Overview**
This workflow automates certificate generation with built-in state management, version control, and data consistency enforcement. It monitors new submissions, validates inputs, detects existing certificates, handles correction scenarios, and ensures that only one valid active certificate exists per register number at any time.

The system implements idempotent behavior and controlled regeneration logic to prevent duplication and data conflicts.

---

## **Workflow Architecture**
Sheet Trigger → Input Normalization → Certificate Existence Check → Conditional State Branching → PDF Generation → Drive Upload → Sharing → Email → Sheet Update → Data Cleanup

---

## **1. Triggers**
- **Google Sheets Trigger** – Activates when a new submission row is added.
- Validates row content using an IF node to prevent empty executions.
- Uses loop control to process rows individually for execution stability.

---

## **2. Core Logic / Agent / Processing**

### Input Normalization
- Cleans name and email fields.
- Standardizes formatting (trim spaces, consistent casing).
- Prevents filename mismatches due to formatting variations.

---

### Certificate Existence Detection
- Searches Google Drive using Register Number.
- Determines one of three states:
  - No existing certificate
  - Certificate exists and matches name
  - Certificate exists but name has changed

---

### Stateful Branch Logic

#### Case 1 – First-Time Creation
- Generate new certificate (PDF)
- Upload to Drive
- Share file
- Send email
- Mark row as `Done`

---

#### Case 2 – Existing Certificate (Name Match)
- Skip regeneration
- Reshare existing file
- Send email
- Update row

This avoids unnecessary processing and preserves system efficiency.

---

#### Case 3 – Data Correction / Name Change
- Delete existing certificate file
- Locate previously completed rows for the same Register Number
- Delete old rows marked as `Done`
- Regenerate certificate
- Upload, share, email, update row

---

## **Why Previous Rows Are Deleted**

The system enforces:

One Register Number → One Active Certificate

Deleting previous rows ensures:

- No duplicate submission history
- No conflicting certificate versions
- No multiple “Done” entries for the same identity
- Clean status tracking
- Stable loop execution
- Accurate re-issuance handling

Without deletion, the workflow could:
- Send outdated certificates
- Create version confusion
- Maintain inconsistent sheet state
- Cause incorrect regeneration behavior

This deletion step acts as controlled version cleanup logic.

---

## **3. Integrated Tools**
- **Google Sheets** – Submission intake, status tracking, row deletion
- **Google Drive (Search, Upload, Delete, Share)** – Certificate lifecycle management
- **HTTP Request (Puppeteer Service)** – Dynamic PDF certificate generation
- **Gmail** – Automated certificate distribution
- **JavaScript Nodes** – Filename comparison and normalization logic
- **IF + Loop Nodes** – Conditional routing and execution control

---

## **Key Features**
- Stateful certificate version management
- Idempotent workflow design
- Duplicate submission handling
- Controlled regeneration logic
- Automated file lifecycle management
- Data cleanup before re-issuance
- Status-based execution control
- Drive-based deduplication
- Safe re-send without regeneration

---

## **Use Cases**
- Academic certificate automation
- Event completion certificates
- Workshop participation certificates
- Institutional certificate issuance systems
- Controlled certificate reissuance workflows

---

## **Technical Stack**
- n8n Workflow Automation
- Google Sheets API
- Google Drive API
- Puppeteer-based PDF Generation Service
- Gmail Integration
- JavaScript Processing Nodes
- Conditional Routing Architecture

---

## **Security & Privacy**
This workflow is showcased using sanitized screenshots only.
All Drive IDs, email configurations, certificate templates, and credentials have been removed.