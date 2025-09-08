 Google Forms to PDF Automation

A Google Apps Script that automatically saves Google Form responses as PDF files into a specified Google Drive folder. This is useful for surveys, feedback forms, HR forms, event registrations, or any workflow where you want to archive responses neatly.

---

## Features

- Automatically triggers when a new Google Form response is submitted.
- Generates a PDF document containing all responses.
- Saves the PDF in a designated Google Drive folder.
- Cleans up temporary Google Docs automatically.
- Easy to set up and customize for any Google Form.

---

## Demo

**Workflow:**

1. User submits a Google Form.
2. Response is recorded in the linked Google Sheet.
3. Apps Script generates a PDF from the response.
4. PDF is saved into the specified Google Drive folder.

---

## Setup Instructions

1. **Create your Google Form** and link it to a Google Sheet (Responses → green Sheets icon).
2. **Open Apps Script** from the response Sheet:
   - Extensions → Apps Script
3. **Paste the script** (`Code.gs`) into the editor.
4. **Set your Google Drive folder ID**:

```javascript



•	The folder ID is found in the URL of your Drive folder: https://drive.google.com/drive/folders/<FOLDER_ID>
	5	Authorize the script:
	◦	Run the helper function testFolderAccess_and_authorize() once.
	◦	Accept permissions for Drive, Docs, and Spreadsheet.
	6	Set up the trigger:
	◦	Go to Triggers (⏰ icon) → Add Trigger
	◦	Function: handleFormSubmit
	◦	Event source: From spreadsheet
	◦	Event type: On form submit
	7	Test:
	◦	Submit a test response through the Google Form.
	◦	Verify the PDF is created in your Drive folder.



