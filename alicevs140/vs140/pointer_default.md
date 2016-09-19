---
title: "pointer_default"
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
ms.assetid: 2d0c7bbc-a1e8-4337-9e54-e304523e2735
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# pointer_default
Specifies the default pointer attribute for all pointers, except top-level pointers that appear in parameter lists.  
  
## Syntax  
  
```  
  
      [ pointer_default(  
   value  
) ]  
```  
  
#### Parameters  
 *value*  
 A value that describes the pointer type: **ptr**, `ref`, or **unique**.  
  
## Remarks  
 The **pointer_default** C++ attribute has the same functionality as the [pointer_default](http://msdn.microsoft.com/library/windows/desktop/aa367141) MIDL attribute.  
  
## Example  
 See the example for [defaultvalue](../vs140/defaultvalue.md) for a sample use of **pointer_default**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|`interface`|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Interface Attributes](../vs140/Interface-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)