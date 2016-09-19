---
title: "helpstring"
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
ms.assetid: 0401e905-a63e-4fad-98d0-d1efea111966
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# helpstring
Specifies a character string that is used to describe the element to which it applies.  
  
## Syntax  
  
```  
  
      [ helpstring(  
   "string"  
) ]  
```  
  
#### Parameters  
 `string`  
 The text of the help string.  
  
## Remarks  
 The **helpstring** C++ attribute has the same functionality as the [helpstring](http://msdn.microsoft.com/library/windows/desktop/aa366856) MIDL attribute.  
  
## Example  
 See the example for [defaultvalue](../vs140/defaultvalue.md) for an example of how to use **helpstring**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|`interface`, `typedef`, **class**, method, property|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Interface Attributes](../vs140/Interface-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [Method Attributes](../vs140/Method-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../vs140/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [helpfile](../vs140/helpfile.md)   
 [helpcontext](../vs140/helpcontext.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)