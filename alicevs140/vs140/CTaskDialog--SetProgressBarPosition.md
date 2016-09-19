---
title: "CTaskDialog::SetProgressBarPosition"
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
ms.assetid: c6c69029-0331-41fe-b4eb-a29c8b0202ab
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetProgressBarPosition
Adjusts the position of the progress bar.  
  
## Syntax  
  
```  
void SetProgressBarPosition(  
   int nProgressPos  
);  
```  
  
#### Parameters  
 [in] `nProgressPos`  
 The position for the progress bar.  
  
## Remarks  
 This method throws an exception with the [ENSURE (MFC)](../vs140/ENSURE--MFC-.md) macro if `nProgressPos` is not in the progress bar range. You can change the progress bar range with [CTaskDialog::SetProgressBarRange](../vs140/CTaskDialog--SetProgressBarRange.md).  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#4)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetProgressBarMarquee](../vs140/CTaskDialog--SetProgressBarMarquee.md)   
 [CTaskDialog::SetProgressBarRange](../vs140/CTaskDialog--SetProgressBarRange.md)   
 [CTaskDialog::SetProgressBarState](../vs140/CTaskDialog--SetProgressBarState.md)