---
title: "CFrameWndEx::OnActivateApp"
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
ms.assetid: 481bc560-8135-46fb-9be9-cd8092c861be
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnActivateApp
Called by the framework when the application is either selected or deselected.  
  
## Syntax  
  
```  
afx_msg void OnActivateApp(  
   BOOL bActive,  
   DWORD dwThreadID  
);  
```  
  
#### Parameters  
 [in] `bActive`  
 `TRUE` if the application is selected; `FALSE` if the application is not selected.  
  
 [in] `dwThreadID`  
 This parameter is not used.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)