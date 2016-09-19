---
title: "CAnimationGroup::m_bAutodestroyAnimationObjects"
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
ms.assetid: 9ca19dfa-1e8a-421f-89f7-26e1c04a89f2
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimationGroup::m_bAutodestroyAnimationObjects
Specifies how to destroy animation objects. If this parameter is TRUE, animation objects will be destroyed automatically when the group is destroyed. Otherwise animation objects must be destroyed manually. The default value is FALSE. Set this value to TRUE only if all animation objects that belong to group are allocated dynamically with operator new.  
  
## Syntax  
  
```  
BOOL m_bAutodestroyAnimationObjects;  
```  
  
## Requirements  
 **Header:** afxanimationcontroller.h  
  
## See Also  
 [CAnimationGroup Class](../vs140/CAnimationGroup-Class.md)