---
title: "importlib"
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
ms.assetid: f129e459-b8d3-4aca-a0bc-ee53e18b62ed
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# importlib
Makes types that have already been compiled into another type library available to the type library being created.  
  
## Syntax  
  
```  
  
      [ importlib(  
   "tlb_file"  
) ];  
```  
  
#### Parameters  
 *tlb_file*  
 The name of a .tlb file, in quotes, that you want imported into the type library of the current project.  
  
## Remarks  
 The **importlib** C++ attribute causes an `importlib` statement to be placed in the library block of the generated .idl file. The **importlib** attribute has the same functionality as the [importlib](http://msdn.microsoft.com/library/windows/desktop/aa367050) MIDL attribute.  
  
## Example  
 The following code shows an example of how to use **importlib**:  
  
```  
// cpp_attr_ref_importlib.cpp  
// compile with: /LD  
[module(name="MyLib")];  
[importlib("importlib.tlb")];  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Anywhere|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [Compiler Attributes](../vs140/Compiler-Attributes.md)   
 [Stand-Alone Attributes](../vs140/Stand-Alone-Attributes.md)   
 [import](../vs140/import.md)   
 [importidl](../vs140/importidl.md)   
 [include](../vs140/include--C---.md)   
 [includelib](../vs140/includelib--C---.md)