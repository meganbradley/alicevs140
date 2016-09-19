---
title: "CFrameWndEx::RecalcLayout"
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
ms.assetid: 92ccdeea-d2d9-426e-a427-196062e81edd
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::RecalcLayout
Adjusts the layout of the frame and its child windows.  
  
## Syntax  
  
```  
virtual void RecalcLayout(  
   BOOL bNotify = TRUE  
);  
```  
  
#### Parameters  
 [in] `bNotify`  
 Specifies whether to notify the OLE client item about the layout change.  
  
## Remarks  
 This method is called when the size of the frame window has changed or when control bars are displayed or hidden.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)