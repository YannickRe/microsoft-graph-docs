---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const team = {
   template@odata.bind:"https://graph.microsoft.com/beta/teamsTemplates('standard')",
   displayName:"My Sample Team",
   description:"My Sample Team’s Description",
   members@odata.bind:[
      {
         @odata.type:"#microsoft.graph.aadUserConversationMember",
         roles:[
            "owner"
         ],
         userId:"0040b377-61d8-43db-94f5-81374122dc7e"
      }
   ]
};

let res = await client.api('/teams')
	.version('beta')
	.post(team);

```