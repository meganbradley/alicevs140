---
title: "custom (C++)"
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
ms.assetid: 3abac928-4d55-4ea6-8cf6-8427a4ad79f1
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# custom (C++)
Defines metadata for an object in the type library.  
  
## Syntax  
  
```  
  
      [ custom(  
   uuid,   
   value  
) ];  
```  
  
#### Parameters  
 *uuid*  
 A unique ID.  
  
 *value*  
 A value that can be put into a variant.  
  
## Remarks  
 The **custom** C++ attribute will cause information to be placed into the type library. You will need a tool that reads the custom value from type library.  
  
 The **custom** attribute has the same functionality as the [custom](http://msdn.microsoft.com/library/windows/desktop/aa366766) MIDL attribute.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Non-COM `interface`, **class**, `enum`s, `idl_module` methods, interface members, interface parameters, `typedef`s, **union**s, `struct`s|  
|**Repeatable**|Yes|  
|**Required attributes**|**coclass** (when used on class)|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Stand-Alone Attributes](../vs140/Stand-Alone-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../vs140/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [Parameter Attributes](../vs140/Parameter-Attributes.md)   
 [Method Attributes](../vs140/Method-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [Interface Attributes](../vs140/Interface-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)