---
title: "CTaskDialog::SetProgressBarMarquee"
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
ms.assetid: eb15d7b3-d89e-46f3-aa93-a25f1f8944ad
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetProgressBarMarquee
Configures a marquee bar for the `CTaskDialog` and adds it to the dialog box.  
  
## Syntax  
  
```  
void SetProgressBarMarquee(  
   BOOL bEnabled = TRUE,  
   int nMarqueeSpeed = 0  
);  
```  
  
#### Parameters  
 [in] `bEnabled`  
 `TRUE` to enable the marquee bar; `FALSE` to disable the marquee bar and remove it from the `CTaskDialog`.  
  
 [in] `nMarqueeSpeed`  
 An integer that indicates the speed of the marquee bar.  
  
## Remarks  
 The marquee bar appears underneath the main text of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md).  
  
 Use `nMarqueeSpeed` to set the speed of the marquee bar; larger values indicate a slower speed. A value of 0 for `nMarqueeSpeed` makes the marquee bar move at the default speed for [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)].  
  
 This method throws an exception with the [ENSURE (MFC)](../vs140/ENSURE--MFC-.md) macro if `nMarqueeSpeed` is less than 0.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#4)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetProgressBarPosition](../vs140/CTaskDialog--SetProgressBarPosition.md)   
 [CTaskDialog::SetProgressBarRange](../vs140/CTaskDialog--SetProgressBarRange.md)   
 [CTaskDialog::SetProgressBarState](../vs140/CTaskDialog--SetProgressBarState.md)