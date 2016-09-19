---
title: "optional (C++)"
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
ms.assetid: 86656a66-8e11-4589-8e30-9b0f34eeed03
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# optional (C++)
Specifies an optional parameter for a member function.  
  
## Syntax  
  
```  
  
[optional]  
  
```  
  
## Remarks  
 The **optional** C++ attribute has the same functionality as the [optional](http://msdn.microsoft.com/library/windows/desktop/aa367132) MIDL attribute.  
  
## Example  
 The following code shows how **optional** might be used:  
  
```  
// cpp_attr_ref_optional.cpp  
// compile with: /LD  
#include "unknwn.h"  
[module(name="ATLFIRELib")];  
  
[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]  
__interface IFireTabCtrl : IDispatch  
{  
   [id(1)] long procedure ([in, optional] VARIANT i);  
};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Interface parameter|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Parameter Attributes](../vs140/Parameter-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)