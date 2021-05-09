# Automated Bill Saving

* From &emsp;| **Outlook.com email**
* To &emsp; &emsp;| **Onedrive**
* Trigger &nbsp;| **When new email arrives**

## Scenario
The provided template extracts the attachment when a new email comes in Outlook.com from Airtel which has the attached monthly bill.  

The bill is then saved to a configured location in Onedrive.

A notification is sent to any mobile which has flow installed and connected to this Microsoft account

_PS: Please not that Microsoft Flow does not support saving of attachments from gmail as of the writing of this post._

## Outcome
The attachment file is saved to the configured location in the below format:  
`<<configured location>>/<<year>>/<<month>>.pdf`

## Assumption
1. Only one attachment is present in the mail.
2. Only one email comes per month

## Connections
1. Outlook.com
2. Onedrive