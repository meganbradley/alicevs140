---
title: "CComControlBase::SetDirty"
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
ms.assetid: 9e3e22c8-9e17-4971-92cf-9cc707ea8664
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::SetDirty
Sets the data member `m_bRequiresSave` to the value in `bDirty`.  
  
## Syntax  
  
```  
  
      void SetDirty(  
   BOOL bDirty   
);  
```  
  
#### Parameters  
 `bDirty`  
 Value of the data member [CComControlBase::m_bRequiresSave](../vs140/CComControlBase--m_bRequiresSave.md).  
  
## Remarks  
 **SetDirty(TRUE)** should be called to flag that the control has changed since it was last saved. The value of `m_bRequiresSave` is retrieved with [CComControlBase::GetDirty](../vs140/CComControlBase--GetDirty.md).  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)