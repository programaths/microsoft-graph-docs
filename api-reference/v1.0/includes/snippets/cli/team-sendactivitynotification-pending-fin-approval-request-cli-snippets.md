---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash

mgc teams send-activity-notification post --team-id {team-id} --body '{\
    "topic": {\
        "source": "entityUrl",\
        "value": "https://graph.microsoft.com/v1.0/teams/{teamId}"\
    },\
    "activityType": "pendingFinanceApprovalRequests",\
    "previewText": {\
        "content": "Internal spending team has a pending finance approval requests"\
    },\
    "recipient": {\
        "@odata.type": "microsoft.graph.aadUserNotificationRecipient",\
        "userId": "569363e2-4e49-4661-87f2-16f245c5d66a"\
    },\
    "templateParameters": [\
        {\
            "name": "pendingRequestCount",\
            "value": "5"\
        }\
    ] \
}\
'

```