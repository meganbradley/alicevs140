---
title: "CWnd::SetIcon"
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
ms.assetid: 5bc2b1a0-a6b6-49f5-a976-a7e56152918e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetIcon
Call this member function to set the handle to a specific icon, as identified by `hIcon`.  
  
## Syntax  
  
```  
  
      HICON SetIcon(  
   HICON hIcon,  
   BOOL bBigIcon   
);  
```  
  
#### Parameters  
 `hIcon`  
 A handle to a previous icon.  
  
 `bBigIcon`  
 Specifies a 32 pixel by 32 pixel icon if **TRUE**; specifies a 16 pixel by 16 pixel icon if **FALSE**.  
  
## Return Value  
 A handle to an icon.  
  
## Remarks  
 When the window class is registered, it selects an icon.  
  
## Example  
 See the example for [CWnd::GetSystemMenu](../vs140/CWnd--GetSystemMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetIcon](../vs140/CWnd--GetIcon.md)