---
title: "&lt;publisherIdentity&gt; Element (ClickOnce Deployment)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-deployment
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 34c579db-d2f2-4b66-b9c8-47207f33d950
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;publisherIdentity&gt; Element (ClickOnce Deployment)
Contains information about the publisher that signed this deployment manifest.  
  
## Syntax  
  
```  
<publisherIdentity  
   name  
   issuerKeyHash  
/>  
```  
  
## Elements and Attributes  
 The `publisherIdentity` element is required for signed manifests. The following table shows the attributes that the `publisherIdentity` element supports.  
  
|Attribute|Description|  
|---------------|-----------------|  
|`name`|Required. Describes the identity of the party that published this application.|  
|`issuerKeyHash`|Required. Contains the SHA-1 hash of the public key of the certificate issuer.|  
  
#### Parameters  
  
## Property Value/Return Value  
  
## Exceptions  
  
## Remarks  
  
## Requirements  
  
## Subhead