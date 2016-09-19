---
title: "CListCtrl::SetView"
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
ms.assetid: 37eb9bda-6fbe-4278-a60d-e7a1fe40f63e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetView
Sets the view of the list view control.  
  
## Syntax  
  
```  
  
      DWORD SetView(  
   int iView   
);  
```  
  
#### Parameters  
 *iView*  
 The view to be selected.  
  
## Return Value  
 Returns 1 if successful, or -1 otherwise. For example, -1 is returned if the view is invalid.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_SETVIEW](http://msdn.microsoft.com/library/windows/desktop/bb761220) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)