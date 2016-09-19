---
title: "aggregatable"
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
ms.assetid: 9253a46a-cd76-41f2-b3b6-86f709bb069c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# aggregatable
Indicates that the class supports aggregation.  
  
## Syntax  
  
```  
  
      [ aggregatable(   
   value  
) ]  
```  
  
#### Parameters  
 *value* (optional)  
 A parameter to indicate when the COM object can be aggregated:  
  
-   **never** The COM object cannot be aggregated.  
  
-   **allowed** The COM object can be created directly or it can be aggregated. This is the default.  
  
-   **always** The COM object cannot be created directly and can only be aggregated. When you call `CoCreateInstance` for this object, you must specify the aggregating object's **IUnknown** interface (the controlling **IUnknown**).  
  
## Remarks  
 The **aggregatable** C++ attribute has the same functionality as the [aggregatable](http://msdn.microsoft.com/library/windows/desktop/aa366721) MIDL attribute. This means that the compiler will pass the **aggregatable** attribute through to the generated .idl file.  
  
 This attribute requires that the [coclass](../vs140/coclass.md), [progid](../vs140/progid.md), or [vi_progid](../vs140/vi_progid.md) attribute (or another attribute that implies one of these) also be applied to the same element. If any single attribute is used, the other two are automatically applied. For example, if **progid** is applied, **vi_progid** and **coclass** are also applied.  
  
 **ATL Projects**  
  
 If this attribute is used within a project that uses ATL, the behavior of the attribute changes. In addition to the previously described behavior, the attribute also adds one of the following macros to the target class:  
  
|Parameter value|Inserted macro|  
|---------------------|--------------------|  
|**Never**|[DECLARE_NOT_AGGREGATABLE](../vs140/DECLARE_NOT_AGGREGATABLE.md)|  
|**Allowed**|[DECLARE_POLY_AGGREGATABLE](../vs140/DECLARE_POLY_AGGREGATABLE.md)|  
|**Always**|[DECLARE_ONLY_AGGREGATABLE](../vs140/DECLARE_ONLY_AGGREGATABLE.md)|  
  
## Example  
  
```  
// cpp_attr_ref_aggregatable.cpp  
// compile with: /LD  
#define _ATL_ATTRIBUTES  
#include "atlbase.h"  
#include "atlcom.h"  
  
[module(name="MyModule")];  
  
[ coclass, aggregatable(allowed),  
  uuid("1a8369cc-1c91-42c4-befa-5a5d8c9d2529")]  
class CMyClass {};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class**, `struct`|  
|**Repeatable**|No|  
|**Required attributes**|One or more of the following: **coclass**, **progid**, or **vi_progid**.|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../vs140/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [Aggregation](http://msdn.microsoft.com/library/windows/desktop/ms686558)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)