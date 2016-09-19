---
title: "VSIXLanguagePack Element (VSIX Language Pack Schema)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 767f5c22-8b87-49ca-92aa-a7a3f026469f
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# VSIXLanguagePack Element (VSIX Language Pack Schema)
Required. Provides the root element for a VSIX language pack. The VSIX language pack provides localized installation information for a VSIX package.  
  
## Syntax  
  
```  
<VSIXLanguagePack>  
  <LocalizedName>...</LocalizedName>  
  <LocalizedDescription>...</LocalizedDescription>  
  <MoreInfoURL>...</MoreInfoURL>  
  <License>...</License>  
</VSIXLanguagePack>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`xmlns`|The XML namespace in which the VSIX Language Pack schema is defined.|  
  
## xmlns Attribute  
  
|Value|Description|  
|-----------|-----------------|  
|`http://schemas.microsoft.com/developer/vsx-schema-lp/2010`|Required. The location of the file that defines the schema for language packs.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[LocalizedName Element](../vs140/LocalizedName-Element--VSIX-Language-Pack-Schema-.md)|Required. The localized name of the extension to be installed.|  
|[LocalizedDescription Element](../vs140/LocalizedDescription-Element--VSIX-Language-Pack-Schema-.md)|Required. The localized description of the extension to be installed.|  
|[MoreInfoURL Element](../vs140/MoreInfoURL-Element--VSIX-Language-Pack-Schema-.md)|Optional. A link to localized information about the extension.|  
|[License Element](../vs140/License-Element--VSIX-Language-Pack-Schema-.md)|Optional. The path of a localized version of the license file for the extension.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|None||  
  
## Element Information  
  
|||  
|-|-|  
|Namespace|http://schemas.microsoft.com/developer/vsx-schema-lp/2010|  
|Schema Name|VSIX Language Pack Schema|  
|Validation File|VSIXLanguagePackSchema.xsd|  
|Can be Empty|No|  
  
## See Also  
 [VSX Schema for Language Packs](../vs140/VSX-Language-Pack-Schema-Reference.md)   
 [Localizing VSIX Packages](../vs140/Localizing-VSIX-Packages.md)   
 [VSIX Extension Schema 1.0 Reference](assetId:///76e410ec-b1fb-4652-ac98-4a4c52e09a2b)