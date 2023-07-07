---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new CustomSecurityAttributeDefinition();
$additionalData = [
		'allowedValues@delta' => $allowedValuesDelta1 = new ();
$		allowedValuesDelta1->setId('Baker');

		$allowedValuesDelta1->setIsActive(false);


$allowedValues@deltaArray []= $allowedValuesDelta1;
$allowedValuesDelta2 = new ();
$		allowedValuesDelta2->setId('Skagit');

		$allowedValuesDelta2->setIsActive(true);


$allowedValues@deltaArray []= $allowedValuesDelta2;
$requestBody->setAllowedValuesDelta($allowedValues@deltaArray);


];
$requestBody->setAdditionalData($additionalData);



$requestConfiguration = new CustomSecurityAttributeDefinitionRequestBuilderPatchRequestConfiguration();
$headers = [
	'OData-Version' => '4.01',
];
$requestConfiguration->headers = $headers;


$result = $graphServiceClient->directory()->customSecurityAttributeDefinitions()->byCustomSecurityAttributeDefinitionId('customSecurityAttributeDefinition-id')->patch($requestBody, $requestConfiguration);


```