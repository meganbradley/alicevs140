---
title: "CWnd::accSelect"
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
ms.assetid: 4c99ce69-4c19-4ead-a92a-33d37fe95611
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::accSelect
Called by the framework to modify the selection or move the keyboard focus of the specified object.  
  
## Syntax  
  
```  
  
      virtual HRESULT accSelect(  
   long flagsSelect,  
   VARIANT varChild  
);  
```  
  
#### Parameters  
 `flagsSelect`  
 Specifies how to change the current selection or focus. See `flagsSelect` in [IAccessible::accSelect](http://msdn.microsoft.com/library/windows/desktop/dd318474) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `varChild`  
 Specifies the object to be selected. This parameter can be either CHILDID_SELF (to select the object itself) or a child ID (to select one of the object's children).  
  
## Return Value  
 Returns S_OK on success, a COM error code on failure. See **Return Values** in **IAccessible::accSelect** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This function is part of MFC's [Active Accessibility](http://msdn.microsoft.com/library/windows/desktop/dd373592) support.  
  
 Override this function in your `CWnd`-derived class if you have nonwindowed user interface elements (other than windowless ActiveX controls, which MFC handles).  
  
 For more information, see [IAccessible::accSelect](http://msdn.microsoft.com/library/windows/desktop/dd318474) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::get_accFocus](../vs140/CWnd--get_accFocus.md)   
 [CWnd::get_accSelection](../vs140/CWnd--get_accSelection.md)