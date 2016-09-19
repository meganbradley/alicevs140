---
title: "CWnd::accDoDefaultAction"
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
ms.assetid: af198d5d-ac2b-4041-a85f-a50a4c93ede9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::accDoDefaultAction
Called by the framework to perform the object's default action.  
  
## Syntax  
  
```  
  
      virtual HRESULT accDoDefaultAction(  
   VARIANT varChild  
);  
```  
  
#### Parameters  
 `varChild`  
 Specifies whether the default action to be invoked is that of the object or one of the object's child elements. This parameter can be either CHILDID_SELF (to perform the object's default action) or a child ID (to perform the default action of one of the object's child elements).  
  
## Return Value  
 Returns S_OK on success, a COM error code on failure. See **Return Values** in [IAccessible::accDoDefaultAction](http://msdn.microsoft.com/library/windows/desktop/dd318470) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 This function is part of MFC's [Active Accessibility](http://msdn.microsoft.com/library/windows/desktop/dd373592) support.  
  
 Override this function in your `CWnd`-derived class to perform your object's default action. For more information, see [IAccessible::accDoDefaultAction](http://msdn.microsoft.com/library/windows/desktop/dd318470) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::EnableActiveAccessibility](../vs140/CWnd--EnableActiveAccessibility.md)