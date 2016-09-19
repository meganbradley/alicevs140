---
title: "Security and Localized Satellite Assemblies"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6d953840-b301-47d5-8d34-30c1b29b5071
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Security and Localized Satellite Assemblies
If your main assembly uses strong naming, satellite assemblies must be signed with the same private key as the main assembly. If the public/private key pair does not match between the main and satellite assemblies, your resources will not be loaded. For more information on signing assemblies, see [How to: Sign an Assembly with a Strong Name](assetId:///2c30799a-a826-46b4-a25d-c584027a6c67).  
  
 In general, you may need to have your organization's signing group or an external signing organization sign with the private key. This is due to the sensitive nature of the private key: access is often restricted to a few individuals. You can use delayed signing during development. For more information, see [Delay Signing an Assembly](assetId:///9d300e17-5bf1-4360-97da-2aa55efd9070).  
  
## See Also  
 [Assembly Security Considerations](assetId:///1b5439c1-f3d5-4529-bd69-01814703d067)   
 [Key Security Concepts](assetId:///3cfced4f-ea02-4e66-ae98-d69286363e98)   
 [Introduction to International Applications Based on the .NET Framework](../vs140/Introduction-to-International-Applications-Based-on-the-.NET-Framework.md)   
 [Localizing Applications](../vs140/Localizing-Applications.md)   
 [Globalizing and Localizing Applications](../Topic/Globalizing%20and%20Localizing%20Applications.md)