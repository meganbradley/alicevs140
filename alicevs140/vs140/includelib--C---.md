---
title: "includelib (C++)"
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
ms.assetid: cd90ea6e-5ae8-4f11-b8d1-662db95412b2
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# includelib (C++)
Causes an .idl or .h file to be included in the generated .idl file.  
  
## Syntax  
  
```  
  
      [ includelib(  
   name.idl  
) ];  
```  
  
#### Parameters  
 *name.idl*  
 The name of the .idl file that you want included as part of the generated .idl file.  
  
## Remarks  
 The `includelib` C++ attribute causes an .idl or .h file to be included in the generated .idl file, after the `importlib` statement.  
  
## Example  
 The following code is shown in a .cpp file:  
  
```  
// cpp_attr_ref_includelib.cpp  
// compile with: /LD  
[module(name="MyLib")];  
[includelib("includelib.idl")];  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Anywhere|  
|**Repeatable**|Yes|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Stand-Alone Attributes](../vs140/Stand-Alone-Attributes.md)   
 [import](../vs140/import.md)   
 [importidl](../vs140/importidl.md)   
 [include](../vs140/include--C---.md)   
 [importlib](../vs140/importlib.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)