# Bug Reports

### Critical
---
<details>
<summary> BUG-001: App crashes when changing theme </summary>

**Severity: Critical**  
**Priority: Highest**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app
2.	Go to Settings
3.	Open Themes
4.	Change current theme

**Expected Result:**
-	Theme changes successfully
- App remains stable
-	Screen is redrawn without crash

**Actual Result:**
-	App crashes while changing theme
-	Log shows: java.lang.RuntimeException: Unable to destroy activity {com.qr.barcode.scanner.oleh/com.qr.barcode.scanner.oleh.MainActivity}at com.qr.barcode.scanner.oleh.MainActivity.onDestroy(MainActivity.kt:435)

**Attachments:**

</details>

### High
---
<details>
<summary> BUG-002: "Generate QR code" button in contact qr generation screen has reduced tap area </summary>

**Severity: High**  
**Priority: High**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app
2.	Go to Generate screen
3.	Tap Contacts
4.	Proceed with contact QR creation
5.	Tap on the edge/side of “Generate QR code” button

**Expected Result:**
-	The entire button surface is tappable
-	Tapping anywhere within the button boundaries triggers the action 

**Actual Result:**
-	Only the text label area registers the tap
-	Tapping the button edges or padding area does nothing
-	Button hit area is significantly smaller than its visual bounds

**Attachments:**

</details>
<details>
<summary> BUG-004: Barcode scanner returns only numeric value instead of product details </summary>

**Severity: High**  
**Priority: Medium**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app 
2.	Scan any product barcode 

**Expected Result:**
-	App retrieves and displays comprehensive product information (name, brand, description, etc.) as described in the app description

**Actual Result:**
-	After scanning, the app displays only the numeric barcode value (raw data) without any additional product information.

**Attachments:**

</details>
<details>
<summary> BUG-014: Error occurs when generating QR with input longer than ~1862 characters </summary>

**Severity: High**  
**Priority: High**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1. Open "URL/Link" section
2. Enter text longer than ~1862 characters
3. Tap "Generate QR"

**Expected Result:**
App handles large input safely:
- Either prevents generation
- QR is generated successfully within supported limits

**Actual Result:**
- App shows an internal error when input exceeds ~1862 characters.  
- No validation or user-friendly message is provided.
- Error log:
04-14 17:22:43.342 W System.err:
at com.qr.barcode.scanner.oleh.ui.ResultImageQrFragment.makeQR(ResultImageQrFragment.kt:213)
at com.qr.barcode.scanner.oleh.ui.ResultImageQrFragment.onCreateView(ResultImageQrFragment.kt:74)

**Attachments:**

</details>


### Medium
---
<details>
<summary> BUG-003: No user feedback after generating and scanning Alarm QR </summary>

**Severity: Medium**  
**Priority: High**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app
2.	Go to Generate screen
3.	Select Alarm
4.	Fill in alarm data
5.	Generate QR
6.	Scan generated QR

**Expected Result:**
-	User receives clear feedback that the alarm has been successfully created
-	Confirmation message, notification, or UI indication is shown
-	User can understand that the action was completed

**Actual Result:**
-	No feedback or confirmation is shown after scanning the QR
-	Alarm may be created, but user is not informed about it
-	User cannot understand whether the action was successful

**Attachments:**

</details>
<details>
<summary> BUG-005: QR generator does not validate input data and allows invalid or malformed payloads </summary>

**Severity: Medium**  
**Priority: Medium**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app
2.	Go to Generate screen
3.	Select URL / Link
4.	Enter random text sequence
5.	Generate QR

**Expected Result:**
-	App should validate input:
    -	reject invalid formats
    -	highlight incorrect fields
    -	prevent QR generation with invalid data
-	Generated QR should represent valid and usable payload

**Actual Result:**
-	App allows generation with invalid or malformed data

**Attachments:**

</details>
<details>
<summary> BUG-006: Open button is displayed for non-URL entries in history </summary>

**Severity: Medium**  
**Priority: Low**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app
2.	Scan or save a QR with non-URL content
3.	Open History
4.	Open result details for that item
5.	Check available action buttons

**Expected Result:**
-	Open button should be shown only for actionable content such as URL
-	Non-URL content should show only relevant actions

**Actual Result:**
-	Open button is displayed even when scanned content is not a URL
**Attachments:**

</details>
<details>
<summary> BUG-009: Confirmation dialog buttons have poor text/background contrast </summary>

**Severity: Medium**  
**Priority: High**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app
2.	Generate any QR code
3.	Tap Generate again
4.	Observe confirmation dialog buttons

**Expected Result:**
-	Button labels should be clearly readable
-	Contrast should meet accessibility and usability standards

**Actual Result:**
-	White text is placed on bright yellow buttons
-	Measured contrast ratio: 1.08:1, which critically fails WCAG 2.1 AA requirement of 4.5:1 for normal text

**Attachments:**

</details>
<details>
<summary> BUG-013: No input length validation in QR generation fields </summary>

**Severity: Medium**  
**Priority: High**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1. Open any QR generation section (Text, Email, SMS, Link/URL, Contact, Phone, WiFi)
2. Enter a very long input (no apparent limit)
3. Observe input behavior

**Expected Result:**
Input is validated:
- Character limit is enforced
OR
- User receives a validation message when exceeding allowed length
  
**Actual Result:**
- No input length restriction is applied.  
- User can enter an unlimited number of characters without any validation or warning.
  
**Attachments:**

</details>


### Low
---
<details>
<summary> BUG-010: Save action provides insufficient feedback </summary>

**Severity: Low**  
**Priority: Low**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app
2.	Generate any QR code
3.	Tap “Save”
4.	Observe app behavior

**Expected Result:**
-	App should clearly confirm that QR was saved, for example:
    -	navigate to History / Saved screen
    -	or visually mark QR as saved
    - or show persistent confirmation
- User should clearly understand that action succeeded

**Actual Result:**
-	Only a short toast message is shown
-	No navigation or visible state change
-	Screen remains the same

**Attachments:**

</details>
<details>
<summary> BUG-012: Insufficient spacing between "PRO features" text and feature blocks </summary>

**Severity: Low**  
**Priority: Low**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1. Open the app
2. Open the PRO subscription screen
3. Observe spacing between "PRO features" text and feature blocks

**Expected Result:**
- There is sufficient spacing between the section title and the feature blocks, ensuring clear visual separation and readability.
  
**Actual Result:**
- Spacing between "PRO features" text and feature blocks is too small, reducing visual clarity and UI hierarchy.
  
**Attachments:**

</details>

### Improvement
---
<details>
<summary> BUG-007: Generated QR result screen contains unrelated buttons and menu shortcuts </summary>

**Severity: Improvement**  
**Priority: Low**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app
2.	Generate any QR code
3.	Review visible action buttons

**Expected Result:**
-	Generated QR result screen should include only relevant actions, such as Save, Share, optional Edit/Color, Generate New
-	Navigation and monetization actions should not distract from core flow

**Actual Result:**
-	Screen contains unrelated buttons such as:
    -	History
    -	Settings
    -	Ads off
    -	Themes
    -	Send to smartwatch

**Attachments:**

</details>
<details>
<summary> BUG-008: QR scanned result screen contains unrelated action buttons </summary>

**Severity: Improvement**  
**Priority: Low**  
**Environment: Google Pixel 8, Android 16**  


**Steps to Reproduce:**
1.	Open the app
2.	Scan any QR code
3.	Review available action buttons

**Expected Result:**
-	Screen should contain only actions relevant to scanned result
-	Example: Open, Copy, Share

**Actual Result:**
-	Screen contains unrelated actions such as:
    - Send to smartwatch
    -	Themes
    -	Ads off
    -	Write to support

**Attachments:**

</details>
<details>
<summary> BUG-011: QR code contrast and density may affect scanning reliability </summary>

**Severity: Improvement**  
**Priority: Low**  


**Steps to Reproduce:**
1. Open the app
2. Create any QR code

**Expected Result:**
- QR code is clearly readable and reliably scannable in all conditions.
**Actual Result:**
- QR code is scannable, but low contrast and density may affect reliability in some conditions.
**Attachments:**

</details>


