---
title: "CustomParameter Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 743c4489-74ac-403a-bbaa-eed7d785a3ac
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CustomParameter Element (Visual Studio Templates)
Contains a custom parameter name and value to use when a project or item is created from the template.  
  
## Syntax  
  
```  
<CustomParameter Name="name" Value="value">  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Name`|Required. The name of the parameter. The format for parameters is $*name*$.|  
|`Value`|Required. The replacement value for the parameter.|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[CustomParameters](../vs140/CustomParameters-Element--Visual-Studio-Templates-.md)|Groups the custom parameters that are to be passed to the template wizard when the wizard makes parameter replacements.|  
  
## Remarks  
 When a template contains `CustomParameter` elements, every instance the `Name` attribute is replaced with the `Value` attribute in the created project or item files.  
  
## Example  
 The following example shows how to use several custom parameters in a template. When a project or item is created from a template with the following custom parameters, all instances of `$color1$` and `$color2$` in the template files will be replaced with `Red` and `Blue`, respectively.  
  
```  
<CustomParameters>  
    <CustomParameter Name="$color1$" Value="Red"/>  
    <CustomParameter Name="$color2$" Value="Blue "/>  
</CustomParameters>  
```  
  
## See Also  
 [CustomParameters Element (Visual Studio Project Templates)](../vs140/CustomParameters-Element--Visual-Studio-Templates-.md)   
 [Parameter Substitution](../vs140/Template-Parameters.md)   
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)