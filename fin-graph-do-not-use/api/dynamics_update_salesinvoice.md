---
title: PATCH salesInvoice method | Microsoft Docs
description: Patches a sales invoice.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen

ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/11/2017
ms.author: solsen
---

# Update salesInvoice
Update the properties of a sales invoices object for Dynamics 365 for Financials.

## HTTP request

```
PATCH /financials/companies/({id})/salesInvoices/({id})
```

## Request headers
|Header|Value|
|------|-----|
|Authorization |Bearer {token}. Required.|
|Content-Type  |application/json|
|If-Match      |Required. When this request header is included and the eTag provided does not match the current tag on the salesInvoice, the salesInvoice will not be updated. |

## Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

## Response
If successful, this method returns a ```200 OK``` response code and an updated salesInvoices object in the response body.

## Example

**Request**

Here is an example of the request.
```json
PATCH https://api.financials.dynamics.com/v1.0/api/beta/companies/({id})/salesInvoices{id}
Content-type: application/json

{
  "paymentTerms": "COD"
}
```

**Response**

Here is an example of the response. 

> [!NOTE]  
>   The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "id-value",
  "number": "1009",
  "invoiceDate": "2015-12-31",
  "dueDate": "2016-01-31",
  "customerPurchaseOrderReference": "",
  "customerId": "customerId-value",
  "contactId": "",
  "customerNumber": "GL00000008",
  "customerName": "GL00000008",
  "billingPostalAddress": {
    "street": "",
    "city": "",
    "state": "",
    "countryLetterCode": "",
    "postalCode": ""
  },
  "currencyCode": "GBP",
  "orderId": "id-value",
  "orderNumber": "",
  "paymentTerms": "COD",
  "shipmentMethod": "",
  "salesperson": "",
  "pricesIncludeTax": false,
  "discountAmount": 0,
  "discountAppliedBeforeTax": true,
  "totalAmountExcludingTax": 6825.6,
  "totalTaxAmount": 682.56,
  "totalAmountIncludingTax": 7508.16,
  "status": "Draft",
  "lastModifiedDateTime": "2017-03-17T19:02:22.043Z"
}
```

## See also
[Working with Dynamics 365 for Financials in Microsoft Graph](../resources/dynamics_overview.md) 