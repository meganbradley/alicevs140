---
title: "CTabCtrl::HitTest"
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
ms.assetid: cb8cda0b-9321-4769-b324-e40a82df1b39
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::HitTest
Determines which tab, if any, is at the specified screen position.  
  
## Syntax  
  
```  
  
      int HitTest(  
  TCHITTESTINFO* pHitTestInfo   
) const;  
```  
  
#### Parameters  
 `pHitTestInfo`  
 Pointer to a [TCHITTESTINFO](http://msdn.microsoft.com/library/windows/desktop/bb760553) structure, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)], which specifies the screen position to test.  
  
## Return Value  
 Returns the zero-based index of the tab or – 1 if no tab is at the specified position.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)