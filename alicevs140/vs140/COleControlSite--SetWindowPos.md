---
title: "COleControlSite::SetWindowPos"
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
ms.assetid: 8ce6c296-613f-4d23-aee7-e3316ed97f58
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::SetWindowPos
Sets the size, position, and Z order of the control site.  
  
## Syntax  
  
```  
  
      virtual BOOL SetWindowPos(  
   const CWnd* pWndInsertAfter,  
   int x,  
   int y,  
   int cx,  
   int cy,  
   UINT nFlags   
);  
```  
  
#### Parameters  
 `pWndInsertAfter`  
 A pointer to the window.  
  
 *x*  
 The new position of the left side of the window.  
  
 *y*  
 The new position of the top of the window.  
  
 `cx`  
 The new width of the window  
  
 `cy`  
 The new height of the window.  
  
 `nFlags`  
 Specifies the window sizing and positioning flags. For possible values, see the Remarks section for [SetWindowPos](http://msdn.microsoft.com/library/windows/desktop/ms633545) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Nonzero if successful, otherwise zero.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)