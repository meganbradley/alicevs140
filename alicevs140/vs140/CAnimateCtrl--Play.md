---
title: "CAnimateCtrl::Play"
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
ms.assetid: e1fc008e-0d6d-4219-9a5e-22a28c4d6be4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimateCtrl::Play
Call this function to play an AVI clip in an animation control.  
  
## Syntax  
  
```  
  
      BOOL Play(  
   UINT nFrom,  
   UINT nTo,  
   UINT nRep   
);  
```  
  
#### Parameters  
 `nFrom`  
 Zero-based index of the frame where playing begins. Value must be less than 65,536. A value of 0 means begin with the first frame in the AVI clip.  
  
 `nTo`  
 Zero-based index of the frame where playing ends. Value must be less than 65,536. A value of – 1 means end with the last frame in the AVI clip.  
  
 *nRep*  
 Number of times to replay the AVI clip. A value of – 1 means replay the file indefinitely.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The animation control will play the clip in the background while your thread continues executing. If the animation control has `ACS_TRANSPARENT` style, the AVI clip will be played using a transparent background rather than the background color specified in the animation clip.  
  
## Example  
 See the example for [CAnimateCtrl::CAnimateCtrl](../vs140/CAnimateCtrl--CAnimateCtrl.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CAnimateCtrl Class](../vs140/CAnimateCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAnimateCtrl::Open](../vs140/CAnimateCtrl--Open.md)   
 [CAnimateCtrl::Stop](../vs140/CAnimateCtrl--Stop.md)   
 [CAnimateCtrl::Seek](../vs140/CAnimateCtrl--Seek.md)   
 [CAnimateCtrl::Create](../vs140/CAnimateCtrl--Create.md)