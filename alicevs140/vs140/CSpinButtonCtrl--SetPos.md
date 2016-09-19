---
title: "CSpinButtonCtrl::SetPos"
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
ms.assetid: 1be7d6d6-f826-4a12-b492-eabdbe3eb9f5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSpinButtonCtrl::SetPos
Sets the current position for a spin button control.  
  
## Syntax  
  
```  
  
      int SetPos(  
   int nPos   
);  
int SetPos32(  
   int nPos   
);  
```  
  
#### Parameters  
 `nPos`  
 New position for the control. This value must be in the range specified by the upper and lower limits for the control.  
  
## Return Value  
 The previous position (16-bit precision for `SetPos`, 32-bit precision for `SetPos32`).  
  
## Remarks  
 `SetPos32` sets the 32-bit position.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSpinButtonCtrl Class](../vs140/CSpinButtonCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSpinButtonCtrl::SetRange](../vs140/CSpinButtonCtrl--SetRange.md)   
 [CSpinButtonCtrl::GetPos](../vs140/CSpinButtonCtrl--GetPos.md)