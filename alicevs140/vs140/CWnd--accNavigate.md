---
title: "CWnd::accNavigate"
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
ms.assetid: 74377c9f-82f8-4df8-b6e5-cdd3c726d6e8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::accNavigate
Called by the framework to traverse to another user interface element within a container and if possible, retrieve the object.  
  
## Syntax  
  
```  
  
      virtual HRESULT accNavigate(  
   long navDir,  
   VARIANT varStart,  
   VARIANT *pvarEndUpAt  
);  
```  
  
#### Parameters  
 `navDir`  
 Specifies the direction to navigate. See `navDir` in [IAccessible::accNavigate](http://msdn.microsoft.com/library/windows/desktop/dd318473) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `varStart`  
 Specifies the starting object. See `varStart` in **IAccessible::accNavigate** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 *pvarEndUpAt*  
 Receives information about the destination user interface object. See *pvarEnd* in **IAccessible::accNavigate** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns S_OK on success, a COM error code on failure. See **Return Values** in **IAccessible::accNavigate** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This function is part of MFC's [Active Accessibility](http://msdn.microsoft.com/library/windows/desktop/dd373592) support.  
  
 Override this function in your `CWnd`-derived class if you have nonwindowed user interface elements (other than windowless ActiveX controls, which MFC handles).  
  
 For more information, see [IAccessible::accNavigate](http://msdn.microsoft.com/library/windows/desktop/dd318473) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::accSelect](../vs140/CWnd--accSelect.md)