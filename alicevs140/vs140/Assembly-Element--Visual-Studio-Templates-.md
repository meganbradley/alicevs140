---
title: "Assembly Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9242f76a-1273-4b8a-8f26-6606f91829ef
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Assembly Element (Visual Studio Templates)
Specifies information about an assembly, which the template uses to add a reference of that assembly to projects.  
  
 <VSTemplate\>  
 <TemplateContent\>  
 <References\>  
 <Reference\>  
 <Assembly\>  
  
## Syntax  
  
```  
<Assembly> AssemblyName </Assembly>  
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
  
 This text specifies the assembly to add to a project when the item template is instantiated. This assembly name must be specified in one of the following ways:  
  
-   As a full assembly name. For example:  
  
    ```  
    <Assembly>  
        MyAssembly, Version=1.0.3300.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a, Custom = null.  
    </Assembly>  
    ```  
  
-   As simple text reference. For example:  
  
    ```  
    <Assembly> System </Assembly>  
    ```  
  
## Remarks  
 `Assembly` is a required child element of `Reference`.  
  
 The `Reference`, `References,` and `Assembly` elements can only be used in .vstemplate files that have a `Type` attribute value of `Item`.  
  
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