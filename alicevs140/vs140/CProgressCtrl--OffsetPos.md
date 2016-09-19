---
title: "CProgressCtrl::OffsetPos"
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
ms.assetid: ac22cae5-09d9-4ee0-b212-d916f23590af
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::OffsetPos
Advances the progress bar control's current position by the increment specified by `nPos` and redraws the bar to reflect the new position.  
  
## Syntax  
  
```  
  
      int OffsetPos(  
   int nPos   
);  
```  
  
#### Parameters  
 `nPos`  
 Amount to advance the position.  
  
## Return Value  
 The previous position of the progress bar control.  
  
## Example  
 [!CODE [NVC_MFC_CProgressCtrl#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CProgressCtrl#5)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CProgressCtrl::SetPos](../vs140/CProgressCtrl--SetPos.md)   
 [CProgressCtrl::SetRange](../vs140/CProgressCtrl--SetRange.md)   
 [CProgressCtrl::StepIt](../vs140/CProgressCtrl--StepIt.md)