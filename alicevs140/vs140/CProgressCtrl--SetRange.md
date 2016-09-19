---
title: "CProgressCtrl::SetRange"
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
ms.assetid: adb494b8-ac8a-4d1f-b953-41944d32cd5a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CProgressCtrl::SetRange
Sets the upper and lower limits of the progress bar control's range and redraws the bar to reflect the new ranges.  
  
## Syntax  
  
```  
  
      void SetRange(  
   short nLower,  
   short nUpper   
);  
void SetRange32(  
   int nLower,  
   int nUpper   
);  
```  
  
#### Parameters  
 `nLower`  
 Specifies the lower limit of the range (default is zero).  
  
 `nUpper`  
 Specifies the upper limit of the range (default is 100).  
  
## Remarks  
 The member function `SetRange32` sets the 32-bit range for the progress control.  
  
## Example  
 [!CODE [NVC_MFC_CProgressCtrl#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CProgressCtrl#8)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CProgressCtrl::OffsetPos](../vs140/CProgressCtrl--OffsetPos.md)   
 [CProgressCtrl::SetPos](../vs140/CProgressCtrl--SetPos.md)   
 [CProgressCtrl::StepIt](../vs140/CProgressCtrl--StepIt.md)