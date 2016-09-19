---
title: "CProgressCtrl::GetPos"
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
ms.assetid: c784969b-7d68-4cee-a031-5ad77a5da04a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::GetPos
Retrieves the current position of the progress bar.  
  
## Syntax  
  
```  
  
int GetPos( );  
  
```  
  
## Return Value  
 The position of the progress bar control.  
  
## Remarks  
 The position of the progress bar control is not the physical location on the screen, but rather is between the upper and lower range indicated in [SetRange](../vs140/CProgressCtrl--SetRange.md).  
  
## Example  
 [!CODE [NVC_MFC_CProgressCtrl#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CProgressCtrl#3)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CProgressCtrl::SetPos](../vs140/CProgressCtrl--SetPos.md)