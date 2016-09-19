---
title: "CSliderCtrl::GetThumbLength"
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
ms.assetid: 756006b9-1d9b-4465-aff5-bc941b39351f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::GetThumbLength
Retrieves the length of the slider in the current trackbar control.  
  
## Syntax  
  
```  
int GetThumbLength() const;  
```  
  
## Return Value  
 The length of the slider, in pixels.  
  
## Remarks  
 This method sends the [TBM_GETTHUMBLENGTH](http://msdn.microsoft.com/library/windows/desktop/bb760201) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TBM_GETTHUMBLENGTH](http://msdn.microsoft.com/library/windows/desktop/bb760201)   
 [CSliderCtrl::SetThumbLength](../vs140/CSliderCtrl--SetThumbLength.md)