---
title: "Reference Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 852772ea-c324-42e9-8c8a-6d565414a109
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Reference Element (Visual Studio Templates)
Specifies the assembly reference to add when the item is added to a project.  
  
 <VSTemplate\>  
 <TemplateContent\>  
 <References\>  
 <Reference\>  
  
## Syntax  
  
```  
<Reference>  
    <Assembly> ... </Assembly>  
</Reference>  
```  
  
## Attributes and Elements  
 The following sections describe attribute, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Assembly](../vs140/Assembly-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Specifies information about an assembly, which the template uses to add a reference of that assembly to projects. There must be one `Assembly` element in every `Reference` element.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[References](../vs140/References-Element--Visual-Studio-Templates-.md)|Groups the assembly references that the template adds to projects.|  
  
## Remarks  
 `Reference` is a required child element of `References`.  
  
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