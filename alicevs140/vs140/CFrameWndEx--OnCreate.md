---
title: "CFrameWndEx::OnCreate"
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
ms.assetid: 3fc84b27-0ea5-4fa1-8c72-7d5b929934e3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnCreate
Called by the framework after the frame is created.  
  
## Syntax  
  
```  
afx_msg int OnCreate(  
   LPCREATESTRUCT lpCreateStruct  
);  
```  
  
#### Parameters  
 [in] `lpCreateStruct`  
 A pointer to the [CREATESTRUCT](../vs140/CREATESTRUCT-Structure.md) for the new frame.  
  
## Return Value  
 0 to continue with the frame creation; -1 to destroy the frame.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)