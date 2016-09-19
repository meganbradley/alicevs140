---
title: "dispinterface"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: 61c5a4a1-ae92-47e9-8ee4-f847be90172b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# dispinterface
Places an interface in the .idl file as a dispatch interface.  
  
## Syntax  
  
```  
  
[dispinterface]  
  
```  
  
## Remarks  
 When the **dispinterface** C++ attribute precedes an interface, it causes the interface to be placed inside the library block in the generated .idl file.  
  
 Unless you specify a base class, a dispatch interface will derive from `IDispatch`. You must specify an [id](../vs140/id.md) for the members of a dispatch interface.  
  
 The usage example for [dispinterface](http://msdn.microsoft.com/library/windows/desktop/aa366802) in the MIDL documentation:  
  
```  
dispinterface helloPro   
   { interface hello; };   
```  
  
 is not valid for the **dispinterface** attribute.  
  
## Example  
 See the example for [bindable](../vs140/bindable.md) for an example of how to use **dispinterface**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|`interface`|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|**dual**, **object**, **oleautomation**, `local`, **ms_union**|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Attributes by Usage](../vs140/Attributes-by-Usage.md)   
 [uuid](../vs140/uuid--C---Attributes-.md)   
 [dual](../vs140/dual.md)   
 [custom](../vs140/custom--C---.md)   
 [object](../vs140/object--C---.md)   
 [__interface](../vs140/__interface.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)