---
title: "References Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1969146d-46bf-422d-8d46-0e9493925003
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# References Element (Visual Studio Templates)
Groups the assembly references that the template adds to projects.  
  
 <VSTemplate\>  
 <TemplateContent\>  
 <References\>  
  
## Syntax  
  
```  
<References>  
    <Reference>... </Reference>  
    <Reference>... </Reference>  
    ...  
</References>  
```  
  
## Attributes and Elements  
 The following sections describe attribute, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Reference](../vs140/Reference-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Specifies the assembly reference to add when the item is added to a project. There must be one or more `Reference` elements in a `References` element.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[TemplateContent](../vs140/TemplateContent-Element--Visual-Studio-Templates-.md)|Specifies the contents of the template.|  
  
## Remarks  
 `References` is an optional child element of `TemplateContent`.  
  
 The `Reference` and `References` elements can only be used in .vstemplate files that have a `Type` attribute value of `Item`.  
  
## Example  
 The following example illustrates the `TemplateContent` element of an item template. This XML adds references to the System.dll and System.Data.dll assemblies.  
  
```  
<TemplateContent>  
    <References>  
        <Reference>  
            <Assembly>  
                System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089  
            </Assembly>  
        </Reference>  
        <Reference>  
            <Assembly>  
                System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089  
            </Assembly>  
        </Reference>  
    </References>  
    ...  
</TemplateContent>  
```  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)