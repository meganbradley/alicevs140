---
title: "CComControlBase::OnKillFocus"
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
ms.assetid: 37ab46f3-0d08-4715-9a36-22b5de1bac5a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::OnKillFocus
Checks that the control is in-place active and has a valid control site, then informs the container that the control has lost focus.  
  
## Syntax  
  
```  
LRESULT OnKillFocus(  
   UINT /* nMsg */,  
   WPARAM /* wParam */,  
   LPARAM /* lParam */,  
   BOOL& bHandled   
);  
```  
  
#### Parameters  
 `nMsg`  
 Reserved.  
  
 `wParam`  
 Reserved.  
  
 `lParam`  
 Reserved.  
  
 `bHandled`  
 Flag that indicates whether the window message was successfully handled. The default is `FALSE`.  
  
## Return Value  
 Always returns 1.  
  
## Requirements  
 `Header:` atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)