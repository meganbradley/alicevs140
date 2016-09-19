---
title: "CTaskDialog::SetProgressBarRange"
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
ms.assetid: 9b6ce5e0-03ff-483d-b7de-d50c630ee946
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetProgressBarRange
Adjusts the range of the progress bar.  
  
## Syntax  
  
```  
void SetProgressBarRange(  
   int nRangeMin,  
   int nRangeMax  
);  
```  
  
#### Parameters  
 [in] `nRangeMin`  
 The lower bound of the progress bar.  
  
 [in] `nRangeMax`  
 The upper bound of the progress bar.  
  
## Remarks  
 The position of the progress bar is relative to `nRangeMin` and `nRangeMax`. For example, if `nRangeMin` is 50 and `nRangeMax` is 100, a position of 75 is halfway across the progress bar. Use [CTaskDialog::SetProgressBarPosition](../vs140/CTaskDialog--SetProgressBarPosition.md) to set the position of the progress bar.  
  
 To display the progress bar, the option `TDF_SHOW_PROGRESS_BAR` must be enabled and `TDF_SHOW_MARQUEE_PROGRESS_BAR` must not be enabled. This method automatically sets `TDF_SHOW_PROGRESS_BAR` and clears `TDF_SHOW_MARQUEE_PROGRESS_BAR`. Use [CTaskDialog::SetOptions](../vs140/CTaskDialog--SetOptions.md) to manually change the options for this instance of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md).  
  
 This method throws an exception with the [ENSURE (MFC)](../vs140/ENSURE--MFC-.md) macro if `nRangeMin` is not less than `nRangeMax`. This method also throws an exception if the `CTaskDialog` is already displayed and has a marquee progress bar.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#4)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetProgressBarPosition](../vs140/CTaskDialog--SetProgressBarPosition.md)   
 [CTaskDialog::SetProgressBarState](../vs140/CTaskDialog--SetProgressBarState.md)   
 [CTaskDialog::SetProgressBarMarquee](../vs140/CTaskDialog--SetProgressBarMarquee.md)