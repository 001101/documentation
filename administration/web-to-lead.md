# Web-to-Lead

## Lead Capture

By utilizing Lead Capture feature administrator can create an entry point for capturing leads through API. Create an entry point at Administration > Lead Capture.

* Subscribe to Target List - Created lead will be added to a specified target list;
* Subscribe Contact if exists - If a contact with the same email exists then contact will be added to the target list;
* Target Team - A team to assign created lead to;
* Campaign - Statystics will be avilable in a campaign log;
* Payload Fields - Select what fields need to be passsed.

### Double Opt-in (confirmed opt-in)

If double opt-in is enabled then your subscribers will need to confirm their intention to opt-in by clicking on a link in an email. An email will be send automatically once data is received through API.

Create Email Template that will be used for a double opt-in. You can use following placeholders in a template body:

* `{optInUrl}` - confirmation URL;
* `{optInLink}` - confirmation link.

A confitmation link will be added automatically if you didn't insert a placeholder in the email template.

## Posting API request

Your web site need to make a POST request to send form data to you CRM. A request doesn't require any authorization. You just need to use a specific URL with an API Key. Infomation about request is available in the side panel on Lead Capture detail view.


### PHP

[API client in PHP](../development/api-client-php.md)

Example:

```php
<?php

require_once('EspoApiClient.php');

$client = new EspoApiClient('https://URL_OF_YOUR_CRM');

$apiKey = 'f1b04885f28ee1a6d55dd203daed68f9';

$formData = [
    'firstName' => $_POST['firstName'],
    'lastName' => $_POST['lastName'],
    'emailAddress' => $_POST['emailAddress']
];

$client->request('POST', 'LeadCapture/' . $apiKey, $formData);

```

### Python

[API client in Python](../development/api-client-python.md)