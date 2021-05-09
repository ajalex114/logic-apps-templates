# Classifier flow

* From &emsp;| **OneDrive**
* To &emsp; &emsp;| **Onedrive, Outlook, CSV**
* Trigger &nbsp;| **When new file is created in Onedrive in specified folder**

## Scenario
This was a POC to classify a picture and process accordingly

This flow is triggered when a new file is created in the specified Onedrive folder (in this case Onedrive Pictures folder).
I have configured camera upload of all pictures taken on my mobile. It means, this flow is triggered every time I take a picture on my mobile.

Cognitive service is used to classify the picture present. In this case, the classifications are 
 1. Milk present
 2. Milk not present

The flow extracts the file contents and posts it to the Cognitive Service. It returns the prediction.
Based on the prediction score, it is determined if Milk is present or not in the picture.

The CSV file is created (if not already existing) per month.
The file content is copied into a variable and the latest value is appended to it (if not already existing).

The image is later moved to a different folder, in case it is classified as a picture with Milk present in it.

An email is sent to the specified email id, mentioning if milk is present or not.

## Outcome
1. CSV is updated with presence of Milk every day
2. Image with Milk is moved to a different folder
3. A mail is sent with the status.

## Assumptions


## Connections
1. Onedrive -> For the trigger, Extracting content of file, Moving file location, Reading CSV file, Creating CSV file, Updating CSV File
2. Azure Cognitive Service
3. Outlook.com