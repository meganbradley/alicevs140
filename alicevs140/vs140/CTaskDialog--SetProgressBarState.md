---
title: "CTaskDialog::SetProgressBarState"
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
ms.assetid: 5442e5d6-2c44-4992-a16b-37eb0ee470fa
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetProgressBarState
Sets the state of the progress bar and displays it on the `CTaskDialog`.  
  
## Syntax  
  
```  
void SetProgressBarState(  
   int nState = PBST_NORMAL  
);  
```  
  
#### Parameters  
 [in] `nState`  
 The state of the progress bar. See the Remarks section for the possible values.  
  
## Remarks  
 This method throws an exception with the [ENSURE (MFC)](../vs140/ENSURE--MFC-.md) macro if the `CTaskDialog` is already displayed and has a marquee progress bar.  
  
 The following table lists the possible values for `nState`. In all these cases, the progress bar will fill with the regular color until it reaches the designated stop position. At that point it will change color based on the state.  
  
 PBST_NORMAL  
 After the progress bar fills, the `CTaskDialog` does not change the color of the bar. By default, the regular color is green.  
  
 PBST_ERROR  
 After the progress bar fills, the `CTaskDialog` changes the color of the bar to the error color. By default, this is red.  
  
 PBST_PAUSED  
 After the progress bar fills, the `CTaskDialog` changes the color of the bar to the paused color. By default, this is yellow.  
  
 You can set where the progress bar stops with [CTaskDialog::SetProgressBarPosition](../vs140/CTaskDialog--SetProgressBarPosition.md).  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#4)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetProgressBarMarquee](../vs140/CTaskDialog--SetProgressBarMarquee.md)   
 [CTaskDialog::SetProgressBarRange](../vs140/CTaskDialog--SetProgressBarRange.md)   
 [CTaskDialog::SetProgressBarPosition](../vs140/CTaskDialog--SetProgressBarPosition.md)