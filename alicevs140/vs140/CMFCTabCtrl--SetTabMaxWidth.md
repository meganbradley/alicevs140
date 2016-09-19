---
title: "CMFCTabCtrl::SetTabMaxWidth"
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
ms.assetid: 9216b77b-2ad9-4d94-88ad-fa80e3b04080
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::SetTabMaxWidth
Specifies the maximum tab width in a tabbed window.  
  
## Syntax  
  
```  
void SetTabMaxWidth(  
   int nTabMaxWidth   
);  
```  
  
#### Parameters  
 [in] `nTabMaxWidth`  
 The maximum tab width, in pixels.  
  
## Remarks  
 Use this method to limit the width of each tab in a tabbed window. This method is useful if tabs have very long labels. The [CMFCTabCtrl](../vs140/CMFCTabCtrl-Class.md) class constructor initializes the maximum tab width to 0, which actually means that the width is not limited.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)