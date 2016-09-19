---
title: "implements_category"
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
ms.assetid: fb162df3-1ebe-43dc-a084-668d7ef8c03f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# implements_category
Specifies the component categories implemented by the target class.  
  
## Syntax  
  
```  
  
      [ implements_category(  
   implements_category="uuid"  
) ]  
```  
  
#### Parameters  
 **implements_category**  
 The ID of the implemented category.  
  
## Remarks  
 The **implements_category** C++ attribute specifies the component categories implemented by the target class. This is done by creating a CATEGORY map and adding separate entries specified by the **implements_category** attribute. For more information, see [What are Component Categories and How Do They Work?](http://msdn.microsoft.com/library/windows/desktop/ms694322).  
  
 This attribute requires that the [coclass](../vs140/coclass.md), [progid](../vs140/progid.md), or [vi_progid](../vs140/vi_progid.md) attribute (or another attribute that implies one of these) also be applied to the same element. If any single attribute is used, the other two are automatically applied. For example, if **progid** is applied, **vi_progid** and **coclass** are also applied.  
  
## Example  
 The following code specifies that the following object implements the Control category.  
  
```  
// cpp_attr_ref_implements_category.cpp  
// compile with: /LD  
#define _ATL_ATTRIBUTES  
#include "atlbase.h"  
#include "atlcom.h"  
  
[module (name="MyLib")];  
[ coclass, implements_category("CATID_Control"),  
  uuid("20a0d0cc-5172-40f5-99ae-5e032f3205ae")]  
class CMyClass {};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class**, `struct`|  
|**Repeatable**|Yes|  
|**Required attributes**|One of the following: **coclass**, **progid**, or **vi_progid**|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [COM Attributes](../vs140/COM-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [IMPLEMENTED_CATEGORY](../vs140/IMPLEMENTED_CATEGORY.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)