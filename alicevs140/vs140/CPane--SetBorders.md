---
title: "CPane::SetBorders"
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
ms.assetid: cd6e08d3-1d69-4d4a-b005-16062924049b
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::SetBorders
Sets the border values of the pane.  
  
## Syntax  
  
```  
void SetBorders(  
    int cxLeft = 0,  
    int cyTop = 0,  
    int cxRight = 0,  
    int cyBottom = 0  
);  
void SetBorders(  
    LPCRECT lpRect  
);  
```  
  
#### Parameters  
 [in] `cxLeft`  
 Specifies the width, in pixels, of the left border of the pane.  
  
 [in] `cyTop`  
 Specifies the width, in pixels, of the top border of the pane.  
  
 [in] `cxRight`  
 Specifies the width, in pixels, of the right border of the pane.  
  
 [in] `cyBottom`  
 Specifies the width, in pixels, of the bottom border of the pane.  
  
 [in] `lpRect`  
 A [CRect](../vs140/CRect-Class.md) object that contains the width, in pixels, of each border of the pane.  
  
## Remarks  
 Call this function to set the sizes of the pane's borders.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)