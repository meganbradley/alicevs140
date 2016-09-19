---
title: "CWnd::accHitTest"
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
ms.assetid: a4f54b11-2717-4592-93e8-138d8cd802b5
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::accHitTest
Called by the framework to retrieve the child element or child object at a given point on the screen.  
  
## Syntax  
  
```  
  
      virtual HRESULT accHitTest(  
   long xLeft,  
   long yTop,  
   VARIANT *pvarChild  
);  
```  
  
#### Parameters  
 `xLeft`  
 X-coordinate of the point to be hit tested (in screen units).  
  
 `yTop`  
 Y-coordinate of the point to be hit tested (in screen units).  
  
 `pvarChild`  
 Receives information identifying the object at the point specified by `xLeft` and `yTop`. See *pvarID* in [IAccessible::accHitTest](http://msdn.microsoft.com/library/windows/desktop/dd318471) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns S_OK on success, a COM error code on failure. See **Return Values** in **IAccessible::accHitTest** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This function is part of MFC's [Active Accessibility](http://msdn.microsoft.com/library/windows/desktop/dd373592) support.  
  
 Override this function in your `CWnd`-derived class if you have nonwindowed user interface elements (other than windowless ActiveX controls, which MFC handles).  
  
 For more information, see [IAccessible::accHitTest](http://msdn.microsoft.com/library/windows/desktop/dd318471) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::accLocation](../vs140/CWnd--accLocation.md)