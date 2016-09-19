---
title: "CMFCBaseTabCtrl::GetTabIcon"
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
ms.assetid: b3d1a54a-8776-47d8-91b9-51348bbb0d79
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::GetTabIcon
Retrieves the icon associated with the specified tab.  
  
## Syntax  
  
```  
virtual UINT GetTabIcon(  
   int iTab  
) const;  
```  
  
#### Parameters  
 [in] `iTab`  
 The zero-based index of the tab.  
  
## Return Value  
 The icon ID for the specified tab if successful; -1 if the index is invalid.  
  
## Remarks  
 The [CMFCBaseTabCtrl](../vs140/CMFCBaseTabCtrl-Class.md) object stores the icons in the internal [CImageList](../vs140/CImageList-Class.md) object.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::SetTabIcon](../vs140/CMFCBaseTabCtrl--SetTabIcon.md)