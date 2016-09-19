---
title: "CProgressCtrl::SetPos"
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
ms.assetid: ce775585-cb97-4463-b11a-1ee3296802a7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::SetPos
Sets the progress bar control's current position as specified by `nPos` and redraws the bar to reflect the new position.  
  
## Syntax  
  
```  
  
      int SetPos(  
   int nPos   
);  
```  
  
#### Parameters  
 `nPos`  
 New position of the progress bar control.  
  
## Return Value  
 The previous position of the progress bar control.  
  
## Remarks  
 The position of the progress bar control is not the physical location on the screen, but rather is between the upper and lower range indicated in [SetRange](../vs140/CProgressCtrl--SetRange.md).  
  
## Example  
 [!CODE [NVC_MFC_CProgressCtrl#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CProgressCtrl#7)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CProgressCtrl::OffsetPos](../vs140/CProgressCtrl--OffsetPos.md)   
 [CProgressCtrl::SetRange](../vs140/CProgressCtrl--SetRange.md)   
 [CProgressCtrl::StepIt](../vs140/CProgressCtrl--StepIt.md)