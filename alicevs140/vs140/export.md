---
title: "export"
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
ms.assetid: 70b3e848-fad6-4e09-8c72-be60ca72a4df
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# export
Causes a data structure to be placed in the .idl file.  
  
## Syntax  
  
```  
  
[export]  
  
```  
  
## Remarks  
 The **export** C++ attribute causes a data structure to be placed in the .idl file and to then be available in the type library in a binary-compatible format that makes it available for use with any language.  
  
 You cannot apply the **export** attribute to a class even if the class only has public members (the equivalent of a `struct`).  
  
 If you export unnamed `enum`s or `struct`s, they will be given names that begin with **__unnamed***x*, where *x* is a sequential number.  
  
 The typedefs valid for export are base types, structs, unions, enums, or type identifiers.  See [typedef](http://msdn.microsoft.com/library/windows/desktop/aa367287) for more information.  
  
## Example  
 The following code shows how to use the **export** attribute:  
  
```  
// cpp_attr_ref_export.cpp  
// compile with: /LD  
[module(name="MyLibrary")];  
  
[export]  
struct MyStruct {  
   int i;  
};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**union**, `typedef`, `enum`, `struct`, or `interface`|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [Compiler Attributes](../vs140/Compiler-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../vs140/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)