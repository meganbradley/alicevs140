---
title: "CComControlBase::m_bRequiresSave"
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
ms.topic: reference
ms.assetid: abfea70d-3352-4e78-819f-abc5fa091853
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_bRequiresSave
Flag indicating the control has changed since it was last saved.  
  
## Syntax  
  
```  
  
unsigned m_bRequiresSave:1;  
```  
  
## Remarks  
 The value of `m_bRequiresSave` can be set with [CComControlBase::SetDirty](../vs140/CComControlBase--SetDirty.md) and retrieved with [CComControlBase::GetDirty](../vs140/CComControlBase--GetDirty.md).  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)