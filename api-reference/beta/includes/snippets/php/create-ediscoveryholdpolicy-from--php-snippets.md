---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new EdiscoveryHoldPolicy();
$requestBody->setDisplayname('My legalHold with sources');

$requestBody->setDescription('Created from Graph API');

$additionalData = [
		'userSources@odata.bind' => $userSourcesOdataBind1 = new ();
$		userSourcesOdataBind1->setOdataType('microsoft.graph.security.userSource');

$		userSourcesOdataBind1->setEmail('SalesTeam@M365x809305.OnMicrosoft.com');


$userSources@odata.bindArray []= $userSourcesOdataBind1;
$requestBody->setUserSourcesOdataBind($userSources@odata.bindArray);


	'siteSources@odata.bind' => $siteSourcesOdataBind1 = new ();
$	siteSourcesOdataBind1->setOdataType('microsoft.graph.security.siteSource');

$siteSourcesOdataBind1Site = new Site();
$	siteSourcesOdataBind1Site->setWebUrl('https://m365x809305.sharepoint.com/sites/Design-topsecret');


$siteSourcesOdataBind1->setSite($siteSourcesOdataBind1Site);

$siteSources@odata.bindArray []= $siteSourcesOdataBind1;
$requestBody->setSiteSourcesOdataBind($siteSources@odata.bindArray);


];
$requestBody->setAdditionalData($additionalData);




$result = $graphServiceClient->security()->cases()->ediscoveryCases()->byEdiscoveryCaseId('ediscoveryCase-id')->legalHolds()->post($requestBody);


```