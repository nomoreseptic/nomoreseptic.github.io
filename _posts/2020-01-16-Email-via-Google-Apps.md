---
layout: post
title: Email via Google Apps Spreadsheet
categories: WEB
---

This function can be utilized by **Google account users** to send automated emails from a Gooogle spreadsheet. Apps Script is a **javascript** based coding language to enhance Google applications and help build new web apps. 

### Create a Sample Automated Email for Practice

1. Your google account is required.
2. Google spreadsheet needs a column with a checkable email (to insure code works when run).
3. Google Script will need permission to access your Gmail account in order to run the script.
4. Script editor for the code is opened by selecting '<> Script editor' in the 'Tools' dropdown atop the spreadsheet.
5. Top 'Untitled' blank is for the script project name.
6. Script 'Save' is in 'File' dropdown.
7.  Select the script function the 'Run function' via 'Run' dropdown menu
8. The editor has handy debugging messages and info to help with fixing coding errors.
9. Check that the Gmail message was received and in desired format.

## Example

![spreadsheet](https://www.keepandshare.com/userpics/h/e/a/r/tnhandstraining/2020-01/sb/screen_shot_2020_01_16_at_1.12.56_pm-778521.jpg?ts=1579209261)

```
function sendEmails() {
  // get the spreadsheet to which this code is connected
  var ss = SpreadsheetApp.getActiveSpreadsheet();
  // get the front sheet of the spreadsheet
  var sheet = ss.getActiveSheet();
  // id the latest row of info at end of spreadsheet
  var lastRow = sheet.getLastRow();
  /* create variables to get cell values needed in the email: getRange method uses row and column numbers to locate these cells.*/
  var discountLink = sheet.getRange(1, 4).getValue();
  var recipient = sheet.getRange(lastRow, 2).getValue();
  var score = sheet.getRange(lastRow, 3).getValue();
  // variable created to ensure 1 and only 1 email is sent
  var emailSent = sheet.getRange(lastRow, 4).getValue();
  // function to send email for newest row
  if (emailSent !== "EMAIL_SENT") {
    // subject line of email
    var subject = 'Sample ';
    // body message of email message
    var body = score + ' out of 100.\nAn 80 or higher is considered passing for this exam.\n' + discountLink;
    // if condn is met, send email
    MailApp.sendEmail(recipient, subject, body);
    // after sending email update this cell value
    var emailColumn = "D";
    ss.getRange(emailColumn + lastRow).setValue("EMAIL_SENT");
    /* ensures that 'EMAIL_SENT' code output and/or effects are written to spreadsheet before continuing */
    SpreadsheetApp.flush();  
  }
}
```
## How I used this script:

This is a linked spreadsheet to a Google form with answers to questions, including the submitter's email, in the columns of the form. I used a time-based "trigger" to run this [script project](https://script.google.com/home/triggers). 

## An added note:

I changed the first line of the script to:

```
function onEdit(e){ //the remaining code lines stay the same
```
This  enables the trigger to be "on change" of the spreadsheet via the 'Edit' dropdown.
