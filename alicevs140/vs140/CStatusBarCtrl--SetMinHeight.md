---
title: "CStatusBarCtrl::SetMinHeight"
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
ms.assetid: 641b6dd0-c9fa-4526-919d-af588c2806dc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBarCtrl::SetMinHeight
Sets the minimum height of a status bar control's drawing area.  
  
## Syntax  
  
```  
  
      void SetMinHeight(  
   int nMin   
);  
```  
  
#### Parameters  
 `nMin`  
 Minimum height, in pixels, of the control.  
  
## Remarks  
 The minimum height is the sum of `nMin` and twice the width, in pixels, of the vertical border of the status bar control.  
  
## Example  
 [!CODE [NVC_MFC_CStatusBarCtrl#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatusBarCtrl#9)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CStatusBarCtrl Class](../vs140/CStatusBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBarCtrl::GetRect](../vs140/CStatusBarCtrl--GetRect.md)   
 [CStatusBarCtrl::GetBorders](../vs140/CStatusBarCtrl--GetBorders.md)