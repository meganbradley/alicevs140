---
title: "CStatusBarCtrl::GetBorders"
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
ms.assetid: 54d49c31-6989-4523-8590-61c060733c55
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::GetBorders
Retrieves the status bar control's current widths of the horizontal and vertical borders and of the space between rectangles.  
  
## Syntax  
  
```  
  
      BOOL GetBorders(  
   int* pBorders   
) const;  
BOOL GetBorders(  
   int& nHorz,  
   int& nVert,  
   int& nSpacing   
) const;  
```  
  
#### Parameters  
 *pBorders*  
 Address of an integer array having three elements. The first element receives the width of the horizontal border, the second receives the width of the vertical border, and the third receives the width of the border between rectangles.  
  
 *nHorz*  
 Reference to an integer that receives the width of the horizontal border.  
  
 *nVert*  
 Reference to an integer that receives the width of the vertical border.  
  
 *nSpacing*  
 Reference to an integer that receives the width of the border between rectangles.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 These borders determine the spacing between the outside edge of the control and the rectangles within the control that contain text.  
  
## Example  
 [!CODE [NVC_MFC_CStatusBarCtrl#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl#2)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::GetParts](../vs140/CStatusBarCtrl--GetParts.md)   
 [CStatusBarCtrl::SetParts](../vs140/CStatusBarCtrl--SetParts.md)