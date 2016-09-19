---
title: "CSpinButtonCtrl::GetAccel"
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
ms.assetid: c196b125-c694-44ae-aeac-6ed460c239d7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSpinButtonCtrl::GetAccel
Retrieves acceleration information for a spin button control.  
  
## Syntax  
  
```  
  
      UINT GetAccel(  
   int nAccel,  
   UDACCEL* pAccel   
) const;  
```  
  
#### Parameters  
 `nAccel`  
 Number of elements in the array specified by `pAccel`.  
  
 `pAccel`  
 Pointer to an array of [UDACCEL](http://msdn.microsoft.com/library/windows/desktop/bb759897) structures that receives acceleration information.  
  
## Return Value  
 Number of accelerator structures retrieved.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSpinButtonCtrl Class](../vs140/CSpinButtonCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSpinButtonCtrl::SetAccel](../vs140/CSpinButtonCtrl--SetAccel.md)