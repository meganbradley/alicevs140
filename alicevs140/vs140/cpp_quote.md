---
title: "cpp_quote"
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
ms.assetid: f75327ff-42bd-498b-9177-7ffa25427e1f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# cpp_quote
Emits the specified string, without the quote characters, into the generated .idl file.  
  
## Syntax  
  
```  
  
      [ cpp_quote(  
   "statement"  
) ];  
```  
  
#### Parameters  
 *statement*  
 A C instruction.  
  
## Remarks  
 The **cpp_quote** C++ attribute is useful if you want to put a preprocessor directive in an .idl file.  
  
 You can also use **cpp_quote** and generate an .h file as part of the MIDL compilation. For example, if you have a C++ header file that uses C++ IDL attributes but cannot use this file for some task, then you can compile it to create a MIDL-generated .h file, which you should be able to use.  
  
 The **cpp_quote** attribute has the same functionality as the [cpp_quote](http://msdn.microsoft.com/library/windows/desktop/aa366765) MIDL attribute.  
  
## Example  
 See the example for [dual](../vs140/dual.md) for an example use how to use **cpp_quote**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Anywhere|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Stand-Alone Attributes](../vs140/Stand-Alone-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)