---
title: "CAtlPreviewCtrlImpl::OnPaint"
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
ms.assetid: 549158c8-04cd-41f5-abc5-cc77d27fb94f
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlPreviewCtrlImpl::OnPaint
Handles the WM_PAINT message.  
  
## Syntax  
  
```  
LRESULT OnPaint(  
   UINT nMsg,  
   WPARAM wParam,  
   LPARAM lParam,  
   BOOL& bHandled  
);  
```  
  
#### Parameters  
 `nMsg`  
 Set to WM_PAINT.  
  
 `wParam`  
 This parameter is not used.  
  
 `lParam`  
 This parameter is not used.  
  
 `bHandled`  
 When this function returns, it contains `TRUE`.  
  
## Return Value  
 Always returns 0.  
  
## Remarks  
  
## Requirements  
 **Header:** atlpreviewctrlimpl.h  
  
## See Also  
 [CAtlPreviewCtrlImpl Class](../vs140/CAtlPreviewCtrlImpl-Class.md)