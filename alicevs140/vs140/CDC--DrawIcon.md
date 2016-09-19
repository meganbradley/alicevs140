---
title: "CDC::DrawIcon"
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
ms.assetid: 58e4c033-e806-4449-b330-a6f91129a578
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::DrawIcon
Draws an icon on the device represented by the current `CDC` object.  
  
## Syntax  
  
```  
  
      BOOL DrawIcon(  
   int x,  
   int y,  
   HICON hIcon   
);  
BOOL DrawIcon(  
   POINT point,  
   HICON hIcon   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the logical x-coordinate of the upper-left corner of the icon.  
  
 *y*  
 Specifies the logical y-coordinate of the upper-left corner of the icon.  
  
 `hIcon`  
 Identifies the handle of the icon to be drawn.  
  
 `point`  
 Specifies the logical x- and y-coordinates of the upper-left corner of the icon. You can pass a [POINT](../vs140/POINT-Structure.md) structure or a [CPoint](../vs140/CPoint-Class.md) object for this parameter.  
  
## Return Value  
 Nonzero if the function completed successfully; otherwise 0.  
  
## Remarks  
 The function places the icon's upper-left corner at the location specified by *x* and *y*. The location is subject to the current mapping mode of the device context.  
  
 The icon resource must have been previously loaded by using the functions `CWinApp::LoadIcon`, `CWinApp::LoadStandardIcon`, or `CWinApp::LoadOEMIcon`. The `MM_TEXT` mapping mode must be selected prior to using this function.  
  
## Example  
 See the example for [CWnd::IsIconic](../vs140/CWnd--IsIconic.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::LoadIcon](../vs140/CWinApp--LoadIcon.md)   
 [CWinApp::LoadStandardIcon](../vs140/CWinApp--LoadStandardIcon.md)   
 [CWinApp::LoadOEMIcon](../vs140/CWinApp--LoadOEMIcon.md)   
 [CDC::GetMapMode](../vs140/CDC--GetMapMode.md)   
 [CDC::SetMapMode](../vs140/CDC--SetMapMode.md)   
 [DrawIcon](http://msdn.microsoft.com/library/windows/desktop/ms648064)   
 [POINT Structure](../vs140/POINT-Structure.md)