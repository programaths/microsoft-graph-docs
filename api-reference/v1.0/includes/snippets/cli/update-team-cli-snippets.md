---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash

mgc teams patch --team-id {team-id} --body '{\
  "memberSettings": {\
    "allowCreateUpdateChannels": true\
  },\
  "messagingSettings": {\
    "allowUserEditMessages": true,\
    "allowUserDeleteMessages": true\
  },\
  "funSettings": {\
    "allowGiphy": true,\
    "giphyContentRating": "strict"\
  }\
}\
'

```