---
title: "CProgressCtrl::SetStep"
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
ms.assetid: d47098e4-ffdf-416e-86df-5ccb26f50532
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::SetStep
Specifies the step increment for a progress bar control.  
  
## Syntax  
  
```  
  
      int SetStep(  
   int nStep   
);  
```  
  
#### Parameters  
 *nStep*  
 New step increment.  
  
## Return Value  
 The previous step increment.  
  
## Remarks  
 The step increment is the amount by which a call to `CProgressCtrl::StepIt` increases the progress bar's current position.  
  
 The default step increment is 10.  
  
## Example  
 [!CODE [NVC_MFC_CProgressCtrl#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CProgressCtrl#9)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CProgressCtrl::OffsetPos](../vs140/CProgressCtrl--OffsetPos.md)   
 [CProgressCtrl::SetPos](../vs140/CProgressCtrl--SetPos.md)   
 [CProgressCtrl::StepIt](../vs140/CProgressCtrl--StepIt.md)   
 [CProgressCtrl::GetStep](../vs140/CProgressCtrl--GetStep.md)