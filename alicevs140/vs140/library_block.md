---
title: "library_block"
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
ms.assetid: ae7a7ebe-5e1a-4eda-a058-11bbd058ece8
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# library_block
Places a construct inside the IDL library block.  
  
## Syntax  
  
```  
  
[library_block]  
  
```  
  
## Remarks  
 When you place a construct inside the library block, you ensure that it will be passed into the type library, regardless of whether it is referenced. By default, only constructs modified by the [coclass](../vs140/coclass.md), [dispinterface](../vs140/dispinterface.md), and [idl_module](../vs140/idl_module.md) attributes are placed in the library block.  
  
## Example  
 In the following code, a custom interface is placed inside the library block.  
  
```  
// cpp_attr_ref_library_block.cpp  
// compile with: /LD  
#include <windows.h>  
[module(name="MyLib")];  
[object, library_block, uuid("9E66A290-4365-11D2-A997-00C04FA37DDB")]  
__interface IMyInterface {  
   HRESULT f1();  
};  
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
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)