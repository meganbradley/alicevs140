---
title: "synchronize"
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
ms.assetid: 15fc8544-955d-4765-b3d5-0f619c8b3f40
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# synchronize
Synchronizes access to the target method.  
  
## Syntax  
  
```  
  
[synchronize]  
  
```  
  
## Remarks  
 The **synchronize** C++ attribute implements support for synchronizing the target method of an object. Synchronization allows multiple objects to use a common resource (such as a method of a class) by controlling the access of the target method.  
  
 The code inserted by this attribute calls the proper `Lock` method (determined by the threading model) at the beginning of the target method. When the method is exited, `Unlock` is automatically called. For more information on these functions, see [CComAutoThreadModule::Lock](../vs140/CComAutoThreadModule--Lock.md)  
  
 This attribute requires that the [coclass](../vs140/coclass.md), [progid](../vs140/progid.md), or [vi_progid](../vs140/vi_progid.md) attribute (or another attribute that implies one of these) also be applied to the same element. If any single attribute is used, the other two are automatically applied. For example, if **progid** is applied, **vi_progid** and **coclass** are also applied.  
  
## Example  
 The following code provides synchronization for the `UpdateBalance` method of the `CMyClass` object.  
  
```  
// cpp_attr_ref_synchronize.cpp  
// compile with: /LD  
#define _ATL_ATTRIBUTES  
#include "atlbase.h"  
#include "atlcom.h"  
  
[module(name="SYNC")];  
  
[coclass,  
 threading(both),  
 vi_progid("MyProject.MyClass"),  
 progid("MyProject.MyClass.1"),  
 uuid("7a7baa0d-59b8-4576-b754-79d07e1d1cc3")  
]  
class CMyClass {  
   float m_nBalance;  
  
   [synchronize]  
   void UpdateBalance(float nAdjust) {  
      m_nBalance += nAdjust;  
   }  
};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Class method, method|  
|**Repeatable**|No|  
|**Required attributes**|One or more of the following: **coclass**, **progid**, or **vi_progid**.|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [COM Attributes](../vs140/COM-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)