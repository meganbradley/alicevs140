---
title: "CMFCVisualManagerOffice2003::SetDefaultWinXPColors"
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
ms.assetid: ad8afc1c-6d69-40f9-a586-f09fe78fccf4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::SetDefaultWinXPColors
Specifies whether the visual manager should use native Windows XP theme colors or colors obtained from [GetSysColor](http://msdn.microsoft.com/library/windows/desktop/ms724371).  
  
## Syntax  
  
```  
static void SetDefaultWinXPColors(  
   BOOL bDefaultWinXPColors = TRUE   
);  
```  
  
#### Parameters  
 [in] `bDefaultWinXPColors`  
 Specifies whether the visual manager will use native Windows XP colors.  
  
## Remarks  
 If `bDefaultWinXPColors` is `TRUE`, the visual manager will use native Windows XP colors such as blue, olive, or silver. Otherwise, the visual manager will use the colors obtained from `GetSysColor`. The visual manager uses visual elements such as `COLOR_3DFACE`, `COLOR_3DSHADOW`, `COLOR_3DHIGHLIGHT`, `COLOR_3DDKSHADOW`, and `COLOR_3DLIGHT`.  
  
 By default, a `CMFCVisualManagerOffice2003` object uses native Windows XP theme colors.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)