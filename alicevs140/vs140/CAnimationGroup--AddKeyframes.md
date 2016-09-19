---
title: "CAnimationGroup::AddKeyframes"
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
ms.assetid: 1269be81-4c7a-465e-9ac1-1a15e786f15e
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationGroup::AddKeyframes
A helper that adds keyframes to a storyboard.  
  
## Syntax  
  
```  
void AddKeyframes(  
   IUIAnimationStoryboard* pStoryboard,  
   BOOL bAddDeep  
);  
```  
  
#### Parameters  
 `pStoryboard`  
 A pointer to a storyboard COM object.  
  
 `bAddDeep`  
 Specifies whether this method should add to the storyboard keyframes that depend on other keyframes.  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationGroup Class](../vs140/CAnimationGroup-Class.md)