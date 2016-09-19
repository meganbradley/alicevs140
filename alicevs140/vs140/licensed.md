---
title: "licensed"
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
ms.assetid: 09cf3b4a-d3f2-43e3-9180-d420333b23bf
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# licensed
Indicates that the COM object to which it applies is licensed, and must be instantiated using **IClassFactory2**.  
  
## Syntax  
  
```  
  
[licensed]  
  
```  
  
## Remarks  
 The **licensed** C++ attribute has the same functionality as the [licensed](http://msdn.microsoft.com/library/windows/desktop/aa367070) MIDL attribute.  
  
## Example  
  
```  
// cpp_attr_ref_licensed.cpp  
// compile with: /LD  
#include "unknwn.h"  
[object, uuid("00000000-0000-0000-0000-000000000001")]  
__interface IMyI : IUnknown {  
   HRESULT f();  
};  
  
[coclass, version("2.1"), uuid(12345678-1111-2222-3333-123456789012),   
licensed, threading(free), progid(some.name)]  
class CSample : public IMyI {  
public:  
   int nSize;  
};  
  
[module(name="MyLibrary", version="1.0", helpstring="My Library Block")];  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class**, `struct`|  
|**Repeatable**|No|  
|**Required attributes**|**coclass**|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)