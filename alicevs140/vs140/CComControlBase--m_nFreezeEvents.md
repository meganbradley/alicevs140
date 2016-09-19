---
title: "CComControlBase::m_nFreezeEvents"
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
ms.assetid: d51b7700-6ec5-46ad-b8e7-ec8431a1f76b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::m_nFreezeEvents
A count of the number of times the container has frozen events (refused to accept events) without an intervening thaw of events (acceptance of events).  
  
## Syntax  
  
```  
  
short m_nFreezeEvents;  
```  
  
## Remarks  
  
> [!NOTE]
>  To use this data member within your control class, you must declare it as a data member in your control class. Your control class will not inherit this data member from the base class because it is declared within a union in the base class.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)   
 [IOleControl::FreezeEvents](http://msdn.microsoft.com/library/windows/desktop/ms678482)