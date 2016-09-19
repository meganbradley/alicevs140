---
title: "CProgressCtrl::StepIt"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 00f03908-ff14-4240-889a-4ebbf4b1c9d8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::StepIt
Advances the current position for a progress bar control by the step increment and redraws the bar to reflect the new position.  
  
## Syntax  
  
```  
  
int StepIt( );  
```  
  
## Return Value  
 The previous position of the progress bar control.  
  
## Remarks  
 The step increment is set by the `CProgressCtrl::SetStep` member function.  
  
## Example  
 [!CODE [NVC_MFC_CProgressCtrl#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CProgressCtrl#10)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CProgressCtrl::SetPos](../vs140/CProgressCtrl--SetPos.md)   
 [CProgressCtrl::SetRange](../vs140/CProgressCtrl--SetRange.md)   
 [CProgressCtrl::SetStep](../vs140/CProgressCtrl--SetStep.md)