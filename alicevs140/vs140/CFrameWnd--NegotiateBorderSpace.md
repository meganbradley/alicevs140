---
title: "CFrameWnd::NegotiateBorderSpace"
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
ms.assetid: 2be37aff-ecd8-4998-ad8e-4ba418c64f5d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::NegotiateBorderSpace
Call this member function to negotiate border space in a frame window during OLE inplace activation.  
  
## Syntax  
  
```  
  
      virtual BOOL NegotiateBorderSpace(  
   UINT nBorderCmd,  
   LPRECT lpRectBorder   
);  
```  
  
#### Parameters  
 *nBorderCmd*  
 Contains one of the following values from the **enum BorderCmd**:  
  
-   **borderGet** = 1  
  
-   **borderRequest** = 2  
  
-   **borderSet** = 3  
  
 `lpRectBorder`  
 Pointer to a [RECT](../vs140/RECT-Structure.md) structure or a [CRect](../vs140/CRect-Class.md) object that specifies the coordinates of the border.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function is the **CFrameWnd** implementation of OLE border space negotiation.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IOleInPlaceUIWindow](http://msdn.microsoft.com/library/windows/desktop/ms680716)