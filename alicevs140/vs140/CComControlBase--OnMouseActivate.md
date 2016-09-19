---
title: "CComControlBase::OnMouseActivate"
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
ms.assetid: dff22f76-c2da-472f-918c-df43cee8b044
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::OnMouseActivate
Checks that the UI is in user mode, then activates the control.  
  
## Syntax  
  
```  
LRESULT OnMouseActivate(  
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