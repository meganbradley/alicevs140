---
title: "CAnimateCtrl::Seek"
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
ms.assetid: dcb8782d-90fa-495d-adca-c8634bc7b5f9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimateCtrl::Seek
Call this function to statically display a single frame of your AVI clip.  
  
## Syntax  
  
```  
  
      BOOL Seek(  
   UINT nTo   
);  
```  
  
#### Parameters  
 `nTo`  
 Zero-based index of the frame to display. Value must be less than 65,536. A value of 0 means display the first frame in the AVI clip. A value of –1 means display the last frame in the AVI clip.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 If the animation control has `ACS_TRANSPARENT` style, the AVI clip will be drawn using a transparent background rather than the background color specified in the animation clip.  
  
## Example  
 See the example for [CAnimateCtrl::CAnimateCtrl](../vs140/CAnimateCtrl--CAnimateCtrl.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CAnimateCtrl Class](../vs140/CAnimateCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAnimateCtrl::Open](../vs140/CAnimateCtrl--Open.md)   
 [CAnimateCtrl::Play](../vs140/CAnimateCtrl--Play.md)   
 [CAnimateCtrl::Create](../vs140/CAnimateCtrl--Create.md)