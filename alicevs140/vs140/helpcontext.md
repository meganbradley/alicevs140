---
title: "helpcontext"
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
ms.assetid: 6fbb022d-a4b7-4989-a02f-7f18a9b0ad96
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# helpcontext
Specifies a context ID that lets the user view information about this element in the Help file.  
  
## Syntax  
  
```  
  
      [ helpcontext(  
   id  
) ]  
```  
  
#### Parameters  
 `id`  
 The context ID of the help topic. See [HTML Help: Context-Sensitive Help for Your Programs](../vs140/HTML-Help--Context-Sensitive-Help-for-Your-Programs.md) for more information on context IDs.  
  
## Remarks  
 The **helpcontext** C++ attribute has the same functionality as the [helpcontext](http://msdn.microsoft.com/library/windows/desktop/aa366851) MIDL attribute.  
  
## Example  
 See the example for [defaultvalue](../vs140/defaultvalue.md) for an example of how to use **helpcontext**.  
  
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
 [helpstring](../vs140/helpstring.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)