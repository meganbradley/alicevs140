---
title: "CMDIFrameWnd::MDITile"
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
ms.assetid: 39db925a-2f13-40c6-9ebc-7e19c679e1a5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWnd::MDITile
Arranges all child windows in a tiled format.  
  
## Syntax  
  
```  
  
      void MDITile( );  
void MDITile(  
   int nType   
);  
```  
  
#### Parameters  
 `nType`  
 Specifies a tiling flag. This parameter can be any one of the following flags:  
  
-   `MDITILE_HORIZONTAL` Tiles MDI child windows so that one window appears above another.  
  
-   `MDITILE_SKIPDISABLED` Prevents disabled MDI child windows from being tiled.  
  
-   `MDITILE_VERTICAL` Tiles MDI child windows so that one window appears beside another.  
  
## Remarks  
 The first version of `MDITile`, without parameters, tiles the windows vertically under Windows versions 3.1 and later. The second version tiles windows vertically or horizontally, depending on the value of the `nType` parameter.  
  
## Example  
 See the example for [CMDIFrameWnd::MDICascade](../vs140/CMDIFrameWnd--MDICascade.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIFrameWnd Class](../vs140/CMDIFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWnd::MDICascade](../vs140/CMDIFrameWnd--MDICascade.md)   
 [CMDIFrameWnd::MDIIconArrange](../vs140/CMDIFrameWnd--MDIIconArrange.md)   
 [WM_MDITILE](http://msdn.microsoft.com/library/windows/desktop/ms644922)