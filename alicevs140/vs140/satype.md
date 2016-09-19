---
title: "satype"
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
ms.assetid: 1716590b-6bcb-4aba-b1bc-82f7335f02c3
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# satype
Specifies the data type of the **SAFEARRAY** structure.  
  
## Syntax  
  
```  
  
      [ satype(  
   data_type  
) ]  
```  
  
#### Parameters  
 *data_type*  
 The data type for the **SAFEARRAY** data structure that is being passed as a parameter to an interface method.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Interface parameter, interface method|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
## Remarks  
 The **satype** C++ attribute specifies the data type of the **SAFEARRAY**.  
  
> [!NOTE]
>  A level of indirection is dropped from the **SAFEARRAY** pointer in the generated .idl file from how it is declared in the .cpp file.  
  
## Example  
  
```  
// cpp_attr_ref_satype.cpp  
// compile with: /LD  
#include "unknwn.h"  
[module(name="MyModule")];  
[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]  
__interface A {  
   [id(1)] HRESULT MyMethod ([in, satype("BSTR")] SAFEARRAY **p);  
};  
```  
  
## See Also  
 [Compiler Attributes](../vs140/Compiler-Attributes.md)   
 [Parameter Attributes](../vs140/Parameter-Attributes.md)   
 [Method Attributes](../vs140/Method-Attributes.md)   
 [id](../vs140/id.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)