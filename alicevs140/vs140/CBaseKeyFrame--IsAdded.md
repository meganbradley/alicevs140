---
title: "CBaseKeyFrame::IsAdded"
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
ms.assetid: 1b7da102-bc97-4494-b5fd-fea6ef562c82
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseKeyFrame::IsAdded
Tells whether a keyframe has been added to storyboard.  
  
## Syntax  
  
```  
BOOL IsAdded() const;  
```  
  
## Return Value  
 TRUE if a keyframe is added to a storyboard; otehrwise FALSE.  
  
## Remarks  
 In the base class IsAdded always returns TRUE, but it's overridden in derived classes.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CBaseKeyFrame Class](../vs140/CBaseKeyFrame-Class.md)