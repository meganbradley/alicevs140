---
title: "CComControlBase::OnPaint"
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
ms.assetid: 34972a7b-245b-48fd-8da1-b697a8a354d9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::OnPaint
Prepares the container for painting, gets the control's client area, then calls the control class's `OnDrawAdvanced` method.  
  
## Syntax  
  
```  
  
      LRESULT OnPaint(  
   UINT /* nMsg */,  
   WPARAM wParam,  
   LPARAM /* lParam */,  
   BOOL& /* lResult */   
);  
```  
  
#### Parameters  
 `nMsg`  
 Reserved.  
  
 `wParam`  
 An existing HDC.  
  
 `lParam`  
 Reserved.  
  
 `lResult`  
 Reserved.  
  
## Return Value  
 Always returns zero.  
  
## Remarks  
 If `wParam` is not NULL, `OnPaint` assumes it contains a valid HDC and uses it instead of [CComControlBase::m_hWndCD](../vs140/CComControlBase--m_hWndCD.md).  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)