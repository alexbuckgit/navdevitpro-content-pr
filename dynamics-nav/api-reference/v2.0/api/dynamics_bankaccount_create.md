---
title: CREATE bankAccounts | Microsoft Docs
description: Creates a bankAccount object in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.service: "dynamics365-business-central"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
---

# Create bankAccounts
Create a bankAccount object in [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)].

## HTTP request
Replace the URL prefix for [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)] depending on environment following the [guideline](../../v2.0/endpoints-apis-for-dynamics.md).
```
POST businesscentralPrefix/companies({id})/bankAccounts
```

## Request headers

|Header         |Value                    |
|---------------|-------------------------|
|Authorization  |Bearer {token}. Required.|
|Content-Type   |application/json         |

## Request body
In the request body, supply a JSON representation of **bankAccounts** object.

## Response
If successful, this method returns ```201 Created``` response code and a **bankAccounts** object in the response body.

## Example

**Request**

Here is an example of a request.

```json
POST https://{businesscentralPrefix}/api/v2.0/companies({id})/bankAccounts
Content-type: application/json

{
    "id": "26049aad-bde4-ea11-bbf2-00155df3a615",
    "number": "NBL",
    "displayName": "New Bank of London"
}
```

**Response**

Here is an example of the response. 

```json
HTTP/1.1 201 Created
Content-type: application/json

{
    "id": "26049aad-bde4-ea11-bbf2-00155df3a615",
    "number": "NBL",
    "displayName": "New Bank of London"
}
```

## See also
[Tips for working with the APIs](/dynamics365/business-central/dev-itpro/developer/devenv-connect-apps-tips)    
[bankaccount](../resources/dynamics_bankaccount.md)    
[Get bankaccount](dynamics_bankaccount_Get.md)    
[Delete bankaccount](dynamics_bankaccount_Delete.md)    
[Update bankaccount](dynamics_bankaccount_Update.md)    