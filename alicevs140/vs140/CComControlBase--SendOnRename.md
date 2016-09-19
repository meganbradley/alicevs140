---
title: "CComControlBase::SendOnRename"
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
ms.assetid: 69ddaf06-6dd5-43ef-82b4-f99acc1ce3d4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::SendOnRename
Notifies all advisory sinks registered with the advise holder that the control has a new moniker.  
  
## Syntax  
  
```  
  
      HRESULT SendOnRename(  
   IMoniker* pmk   
);  
```  
  
#### Parameters  
 *pmk*  
 Pointer to the new moniker of the control.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 Sends a notification that the moniker for the control has changed.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [CComControlBase::m_spOleAdviseHolder](../vs140/CComControlBase--m_spOleAdviseHolder.md)