# e-Transfer Logger
Automated deposit logger for e-Transfers

## Overview
This automation has two parts:
1. a Gmail filter that applies a label to e-transfer confirmations.
2. a Google AppScript that is attached to a google sheet to store the collected information

## Requirements
- You must have Auto Deposit enabled for your e-transfer email.
- You must use a gmail or google workspace account and keep the program files in your associated google drive.

## Setup
1. Make copy of the [file](https://docs.google.com/spreadsheets/d/1ZHWoGJVs9VAnQnTFYOWB8qB5b8IEeyKxo952mIoAckU/edit?usp=sharing). Save the file in a folder somewhere in your google drive.
2. In your gmail:
  - Go to Settings > All settings > Filters and blocked > Import filters
  - Upload the 'mailFilters.xml' file
  - Click 'Open' then 'Create filter'
3. In your copy of the 'Deposit Log' sheet:
  - Go to Extensions > Apps Script and open the apps script
  - In the editor, update DATA_FILE_ID to the google drive ID of your log sheet
  - Optionally you can choose to run it from dropdown Actions > Scan new deposits, or go to the triggers tab and create a time-driven trigger that runs 'scanNewDeposits()' every hour
