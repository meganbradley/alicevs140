---
title: "CReBarCtrl::HitTest"
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
ms.assetid: 1118a341-df6e-49b4-bc2c-53adc4c20756
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::HitTest
Implements the behavior of the Win32 message [RB_HITTEST](http://msdn.microsoft.com/library/windows/desktop/bb774494), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      int HitTest(  
   RBHITTESTINFO* prbht   
);  
```  
  
#### Parameters  
 *prbht*  
 A pointer to a [RBHITTESTINFO](http://msdn.microsoft.com/library/windows/desktop/bb774391) structure. Before sending the message, the **pt** member of this structure must be initialized to the point that will be tested, in client coordinates.  
  
## Return Value  
 The zero-based index of the band at the given point, or -1 if no rebar band was at the point.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)