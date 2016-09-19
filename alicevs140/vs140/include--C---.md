---
title: "include (C++)"
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
ms.assetid: d23f8b91-fe5b-48fa-9371-8bd73af7b8e3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# include (C++)
Specifies one or more header files to be included in the generated .idl file.  
  
## Syntax  
  
```  
  
      [ include(  
   header_file  
) ];  
```  
  
#### Parameters  
 *header_file*  
 The name of a file that you want included in the generated .idl file.  
  
## Remarks  
 The **include** C++ attribute causes an `#include` statement to be placed below the `import "docobj.idl"` statement in the generated .idl file.  
  
 The **include** C++ attribute has the same functionality as the [include](http://msdn.microsoft.com/library/windows/desktop/aa367052) MIDL attribute.  
  
## Example  
 The following code shows an example of how to use **include**. For this example, the file include.h contains only a #include statement.  
  
```  
// cpp_attr_ref_include.cpp  
// compile with: /LD  
[module(name="MyLib")];  
[include(cpp_attr_ref_include.h)];  
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
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Stand-Alone Attributes](../vs140/Stand-Alone-Attributes.md)   
 [import](../vs140/import.md)   
 [importidl](../vs140/importidl.md)   
 [includelib](../vs140/includelib--C---.md)   
 [importlib](../vs140/importlib.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)