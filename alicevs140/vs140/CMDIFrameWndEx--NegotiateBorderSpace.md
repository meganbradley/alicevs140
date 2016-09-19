---
title: "CMDIFrameWndEx::NegotiateBorderSpace"
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
ms.assetid: edd72620-46cb-4a4c-a998-e65fba4cd194
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::NegotiateBorderSpace
Negotiates border space in a frame window during OLE in-place activation.  
  
## Syntax  
  
```  
virtual BOOL NegotiateBorderSpace(  
   UINT nBorderCmd,  
   LPRECT lpRectBorder  
);  
```  
  
#### Parameters  
 [in] `nBorderCmd`  
 Contains one of the following values from the enum `CFrameWnd::BorderCmd`:  
  
-   `borderGet` = 1  
  
-   `borderRequest` = 2  
  
-   `borderSet` = 3  
  
 [in, out] `lpRectBorder`  
 Pointer to a [RECT Structure](../vs140/RECT-Structure.md) or a [CRect Class](../vs140/CRect-Class.md) object that specifies the coordinates of the border.  
  
## Return Value  
 Nonzero if the method was successful; otherwise 0.  
  
## Remarks  
 This method is an implementation of OLE border space negotiation.  
  
## Requirements  
 **Header:** afxmdiframewndex.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)