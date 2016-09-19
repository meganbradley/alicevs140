---
title: "CMFCTabCtrl::GetDocumentIcon"
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
ms.assetid: e6cf1977-55bf-4d37-a2fc-0c9ff731abe4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::GetDocumentIcon
Retrieves the image that is associated with a tab in a pop-up menu of tabbed windows.  
  
## Syntax  
  
```  
static HICON __stdcall GetDocumentIcon(  
   UINT nCmdID  
);  
```  
  
#### Parameters  
 [in] `nCmdID`  
 The command ID of a tab in a pop-up menu of tabbed windows.  
  
## Return Value  
 The handle of a bitmap image.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCTabCtrl::EnableTabDocumentsMenu](../vs140/CMFCTabCtrl--EnableTabDocumentsMenu.md)