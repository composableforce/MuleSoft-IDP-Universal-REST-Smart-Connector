# MuleSoft IDP Universal 🌐 REST Smart Connector 🔌

One Connector to Rule them All

  mediaType: application/json

  protocols: HTTPS

  securedBy: 🛡️ MuleSoft Connected App OAuth 2.0

| Author | Date | Description
  | -------- | ------- | ------- |
  | G.Jeffcock | 23rd June 2024 | Launched|
  ||||
  ||||

  **MuleSoft IDP Universal 🌐 REST Smart Connector 🔌**

  When [Integrating IDP with Anypoint Studio](https://docs.mulesoft.com/idp/integrating-idp-with-anypoint-studio), it's important to consider a few potential challenges, which the MuleSoft IDP Universal 🌐 REST Smart Connector 🔌 is designed to mitigate:

  _📍 Connector Sprawl:_

  **Challenge**: Every published action creates a new connector, leading to an overwhelming number of connectors.

  **Solution**: The Universal REST Connector consolidates these actions, significantly reducing the number of connectors required.

  _📍 Reconfiguration Overload:_

  **Challenge**: Each document action version generates a different connector, necessitating frequent reconfigurations in Anypoint projects.

  **Solution**: By using a single connector, you minimize the need for constant reconfiguration, streamlining project management.

  _📍 Support for Undocumented Functionality:_

  **Challenge**: Integrations often need to support functionalities that aren't well-documented.

  **Solution**: The Universal REST Connector is designed to handle undocumented functionalities, providing more robust and flexible integration capabilities.

  _📍 Rapid Onboarding for Enterprise Scale:_

  **Challenge**: Creating a universal solution that processes and calls at an enterprise scale requires the ability to quickly onboard new document actions.

  **Solution**: This connector allows for the rapid onboarding of new document actions, enabling your enterprise to scale efficiently and effectively.
  
  Resources:
  ![image](https://github.com/user-attachments/assets/7db6772a-5d51-4656-b124-5698bae30f25)

<img width="665" alt="image" src="https://github.com/user-attachments/assets/46865dd1-933b-41d5-a610-7165b1a64e4f">


Implementation:

**Step1** - Save a local copy of the <a href="https://github.com/composableforce/MuleSoft-IDP-Universal-REST-Smart-Connector/blob/main/mulesoft-idp-universal-rest-smart-connector.raml" title="https://github.com/composableforce/MuleSoft-IDP-Universal-REST-Smart-Connector/blob/main/mulesoft-idp-universal-rest-smart-connector.raml" target="_blank">https://github.com/composableforce/MuleSoft-IDP-Universal-REST-Smart-Connector/blob/main/mulesoft-idp-universal-rest-smart-connector.raml</a>

**Step2** - Save a local copy of the <a href="https://github.com/composableforce/MuleSoft-IDP-Universal-REST-Smart-Connector/blob/main/mulesoft-idp-universal-rest-smart-connector.jar" title="https://github.com/composableforce/MuleSoft-IDP-Universal-REST-Smart-Connector/blob/main/mulesoft-idp-universal-rest-smart-connector.jar" target="_blank">https://github.com/composableforce/MuleSoft-IDP-Universal-REST-Smart-Connector/blob/main/mulesoft-idp-universal-rest-smart-connector.jar</a> to see how to use the REST Connector

![image](https://github.com/user-attachments/assets/782c8827-9c53-4337-8824-bba8f93f3fa3)


**Step3** - Create your own version of the RAML Spec in Design Center

![image](https://github.com/user-attachments/assets/73d2946f-5894-4d22-9c02-a1e5f0bdcbdd)


**Step4** - Make changes like adding your MuleSoft Anypoint Org Id

![image](https://github.com/user-attachments/assets/3e36e835-5cd3-49ca-9aa8-255f1f672d63)


Add the dependency Rest Connect Library V1.0.2 if not avlaible like in EMEA (been reported it is missing)  then V1.0.0 will do just change the RAML uses statement

![image](https://github.com/user-attachments/assets/edf78e81-bab7-4698-ae7f-c25aad3ccbb9)


**Step5** - Publish to your Exchange and add colour to your exchange asset:

1. Add Exchange Icon ![image](https://github.com/user-attachments/assets/818704fb-16d3-4d46-871d-a171dd024821)

2. Change Title to “MuleSoft IDP Universal 🌐 REST Smart Connector 🔌”
3. Add Description “One Connector to Rule them All”
4. Add following markdown to Exchange home page

```
![https://blogs.mulesoft.com/wp-content/uploads/IDP-Blog-Image-1.png](https://blogs.mulesoft.com/wp-content/uploads/IDP-Blog-Image-1.png)
```

**Step6** - Import MuleSoft IDP Universal 🌐 REST Smart Connector 🔌 as a dependency into your test Anypoint Studio project to start learning

**Step7** - You can change the REST connector icon

- Apple Mac: To see hidden folder structure beyond and including **.mule** press shift cmd period
- Apple Mac: Find /Users/gjeffcock/AnypointStudio/studio-workspace/718/composableforce/**.mule**/plugins-tmp/repository/7.18.1/eca25329-9592-4ff1-9054-1b08d103b991/mule-plugin-mulesoft-idp-universal-rest-connector/1.0.0
<img width="662" alt="image" src="https://github.com/user-attachments/assets/320461e8-13c9-43fb-ae46-45ea7d1b1d4c">

Now you should have for your pleasure and audiences:
![image](https://github.com/user-attachments/assets/4c95bafa-0bd5-44dc-b0e9-0461201829ff)


**Step8** - Your configuration properties file will require:

```
anypoint.idp.host=idp-rt.us-east-1.anypoint.mulesoft.com
anypoint.idp.basePath=/api/v1
anypoint.idp.port=443
anypoint.idp.protocol=HTTPS
anypoint.idp.responseTimeout=30000

// Connected App https://docs.mulesoft.com/idp/automate-document-processing-with-the-idp-api#create-a-connected-app
anypoint.idp.clientId=9xxxxxxxxxxxxxxxxxxx4
anypoint.idp.clientSecret=9xxxxxxxxxxxxxxxE
anypoint.idp.accessTokenUrl=https://anypoint.mulesoft.com/accounts/api/v2/oauth2/token
anypoint.orgId=3a9b4984-4b75-4c42-8d1b-434f8a5da342
anypoint.idp.callbackURL=https://eoz5chj9g7d68t4.m.pipedream.net
anypoint.idp.callbackURL.apikey=354345345345
anypoint.idp.actionId=9026458a-868d-40b6-90e0-6e80639e0aea
anypoint.idp.actionVersion=1.3.0
anypoint.idp.filenameAndExtension=IDP-PO-CD656092-BurlingtonTextiles.pdf


// Required if you want to use:
// 🌐 IDP - ReviewTask - List
// 🌐 IDP - ReviewTaskByExecution - Fetch
// 🌐 IDP - ReviewTaskByExecution - Update
anypoint.login.username=myAnypointLoginUser
anypoint.login.password=myAnypointLoginPassword
```

Optional but Advisable configuration properties settings:

```
// MuleSoft IDP Universal 🌐 Callback API
// see https://docs.mulesoft.com/idp/automate-document-processing-with-the-idp-api#callback-url

anypoint.apikey=ODZxxxxxxxxxxxxxxxxxxxxxxxx2OGY=
anypoint.idp.callbackURL=https://mulesoft-idp-universal-service-app-fva5e1.5sc6y6-2.usa-e2.cloudhub.io/api/v1/idp/callback
```

**Step9** - Global Element

```
<mule-soft-idp-universal-rest-smart-connector:config
        name="MuleSoft_IDP_Universal_REST_Smart_Connector_Config"
        doc:name="MuleSoft IDP Universal 🌐 REST Smart Connector 🔌 Config"
        doc:id="aebaadbc-9222-44b1-bed1-df2954d6a252"
        property_port="${anypoint.idp.port}"
        property_host="${anypoint.idp.host}"
        property_basePath="${anypoint.idp.basePath}"
        property_protocol="${anypoint.idp.protocol}"
        property_responseTimeout="${anypoint.idp.responseTimeout}"
        property_client-id="${anypoint.idp.clientId}"
        property_client-secret="${anypoint.idp.clientSecret}"
        property_access-token-url="${anypoint.idp.accessTokenUrl}" />
```

![https://blogs.mulesoft.com/wp-content/uploads/IDP-Blog-Image-1.png](https://blogs.mulesoft.com/wp-content/uploads/IDP-Blog-Image-1.png)
