---
title: "pragma"
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
ms.assetid: 3f90d023-b8b5-4007-8311-008bb72cbea1
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# pragma
Emits the specified string into the generated .idl file without the use of  quotation marks. .  
  
## Syntax  
  
```  
  
      [ pragma(  
   pragma_statement  
) ];  
```  
  
#### Parameters  
 *pragma_statement*  
 The pragma that you want to go into the generated .idl file.  
  
## Remarks  
 The **pragma** C++ attribute has the same functionality as the [pragma](http://msdn.microsoft.com/library/windows/desktop/aa367143) MIDL attribute.  
  
## Example  
  
```  
// cpp_attr_ref_pragma.cpp  
// compile with: /LD  
#include "unknwn.h"  
[module(name="MyLib")];  
[pragma(pack(4))];  
  
[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]  
__interface A  
{  
   [id(1)] HRESULT MyMethod ([in, satype("BSTR")] SAFEARRAY **p);  
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
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Stand-Alone Attributes](../vs140/Stand-Alone-Attributes.md)   
 [pack](../vs140/pack.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)