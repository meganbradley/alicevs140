---
title: "CStatusBarCtrl::SetParts"
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
ms.assetid: f7598715-328b-4184-a8bf-04fa01b42860
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::SetParts
Sets the number of parts in a status bar control and the coordinate of the right edge of each part.  
  
## Syntax  
  
```  
  
      BOOL SetParts(  
   int nParts,  
   int* pWidths   
);  
```  
  
#### Parameters  
 `nParts`  
 Number of parts to set. The number of parts cannot be greater than 255.  
  
 *pWidths*  
 Address of an integer array having the same number of elements as parts specified by `nParts`. Each element in the array specifies the position, in client coordinates, of the right edge of the corresponding part. If an element is – 1, the position of the right edge for that part extends to the right edge of the control.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CStatusBarCtrl#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl#10)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::GetBorders](../vs140/CStatusBarCtrl--GetBorders.md)   
 [CStatusBarCtrl::GetParts](../vs140/CStatusBarCtrl--GetParts.md)