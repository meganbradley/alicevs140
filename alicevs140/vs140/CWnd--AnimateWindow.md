---
title: "CWnd::AnimateWindow"
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
ms.assetid: 75adf230-b30f-443c-939e-b02df551bdef
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::AnimateWindow
Produces special effects when showing or hiding windows.  
  
## Syntax  
  
```  
  
      BOOL AnimateWindow(  
   DWORD dwTime,  
   DWORD dwFlags  
);  
```  
  
#### Parameters  
 *dwTime*  
 Specifies how long it takes to play the animation, in milliseconds. Typically, an animation takes 200 milliseconds to play.  
  
 `dwFlags`  
 Specifies the type of animation. For a full list of possible values, see [AnimateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632669).  
  
## Return Value  
 Nonzero if the function succeeds; otherwise 0.  
  
## Remarks  
 This member function emulates the functionality of the function [AnimateWindow](http://msdn.microsoft.com/library/windows/desktop/ms632669), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)