---
title: "CSliderCtrl::GetChannelRect"
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
ms.assetid: 5d0a4f8e-61e7-46b9-ba4a-e97c4fdef1a2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::GetChannelRect
Retrieves the size and position of the bounding rectangle for a slider control's channel.  
  
## Syntax  
  
```  
  
      void GetChannelRect(  
   LPRECT lprc   
) const;  
```  
  
#### Parameters  
 `lprc`  
 A pointer to a [CRect](../vs140/CRect-Class.md) object that contains the size and position of the channel's bounding rectangle when the function returns.  
  
## Remarks  
 The channel is the area over which the slider moves and which contains the highlight when a range is selected.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::GetThumbRect](../vs140/CSliderCtrl--GetThumbRect.md)