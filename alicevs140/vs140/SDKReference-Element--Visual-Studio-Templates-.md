---
title: "SDKReference Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 72c8b352-0b7a-42b3-ba5d-2a2d1e90c34b
caps.latest.revision: 7
translation.priority.mt: 
  - de-de
  - ja-jp
---
# SDKReference Element (Visual Studio Templates)
Specifies that the item template uses an SDK reference.  
  
## Syntax  
  
```xml  
<VSTemplate>      
    <TemplateContent>          
        <References>              
            <Reference>  
                <SDKReference>SDKname</SDKReference>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Reference](../vs140/Reference-Element--Visual-Studio-Templates-.md)|Specifies the assembly reference to add when the item is added to a project.|  
  
## Text Value  
 A text value is required.  
  
## Remarks  
 This text specifies the SDK reference to add to a project when the item template is instantiated.  
  
```xml  
<VSTemplate Version="3.0.0" xmlns="http://schemas.microsoft.com/developer/vstemplate/2005" Type="Item">   
    <TemplateData> . . . </TemplateData>   
    <TemplateContent>   
        <References>   
            <Reference>   
                <SDKReference>Microsoft Visual C++ Runtime Package, Version=11.0.0.0</SDKReference>  
...  
```  
  
## See Also  
 [References Element (Visual Studio Templates)](../vs140/References-Element--Visual-Studio-Templates-.md)   
 [Reference Element (Visual Studio Templates)](../vs140/Reference-Element--Visual-Studio-Templates-.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)   
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)