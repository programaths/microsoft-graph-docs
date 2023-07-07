---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($tokenRequestContext, $scopes);

$requestBody = new InvitePostRequestBody();
$participantsInvitationParticipantInfo1 = new InvitationParticipantInfo();
$participantsInvitationParticipantInfo1->setOdataType('#microsoft.graph.invitationParticipantInfo');

$participantsInvitationParticipantInfo1Identity = new IdentitySet();
$participantsInvitationParticipantInfo1Identity->setOdataType('#microsoft.graph.identitySet');

$additionalData = [
		'phone' => $participantsInvitationParticipantInfo1Identity = new Phone();
$		participantsInvitationParticipantInfo1Identity->setOdataType('#microsoft.graph.identity');

$		participantsInvitationParticipantInfo1Identity->setId('+12345678901');


$participantsInvitationParticipantInfo1Identity->setPhone($phone);

];
$participantsInvitationParticipantInfo1Identity->setAdditionalData($additionalData);



$participantsInvitationParticipantInfo1->setIdentity($participantsInvitationParticipantInfo1Identity);

$participantsArray []= $participantsInvitationParticipantInfo1;
$requestBody->setParticipants($participantsArray);


$requestBody->setClientContext('f2fa86af-3c51-4bc2-8fc0-475452d9764f');



$result = $graphServiceClient->communications()->calls()->byCallId('call-id')->participants()->invite()->post($requestBody);


```