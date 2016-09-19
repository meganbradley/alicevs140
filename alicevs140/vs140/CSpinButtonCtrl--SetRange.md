---
title: "CSpinButtonCtrl::SetRange"
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
ms.assetid: e7e32460-9772-4cf8-9a36-45a3a1800bf5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSpinButtonCtrl::SetRange
Sets the upper and lower limits (range) for a spin button control.  
  
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
 `nLower`and `nUpper`  
 Upper and lower limits for the control. For `SetRange`, neither limit can be greater than **UD_MAXVAL** or less than **UD_MINVAL**; in addition, the difference between the two limits cannot exceed **UD_MAXVAL**. `SetRange32` places no restrictions on the limits; use any integers.  
  
## Remarks  
 The member function `SetRange32` sets the 32-bit range for the spin button control.  
  
> [!NOTE]
>  The default range for the spin button has the maximum set to zero (0) and the minimum set to 100. Because the maximum value is less than the minimum value, clicking the up arrow will decrease the position and clicking the down arrow will increase it. Use `CSpinButtonCtrl::SetRange` to adjust these values.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSpinButtonCtrl Class](../vs140/CSpinButtonCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSpinButtonCtrl::GetRange](../vs140/CSpinButtonCtrl--GetRange.md)   
 [CSpinButtonCtrl::GetPos](../vs140/CSpinButtonCtrl--GetPos.md)   
 [Using CSpinButtonCtrl](../vs140/Using-CSpinButtonCtrl.md)