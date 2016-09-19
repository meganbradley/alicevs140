---
title: "CLinkCtrl::HitTest"
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
ms.assetid: b70c23f0-d41f-45e3-9b4b-baeed979cc7b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLinkCtrl::HitTest
Determines if the user clicked the specified link.  
  
## Syntax  
  
```  
  
      BOOL HitTest(  
   PLHITTESTINFO phti  
) const;  
```  
  
#### Parameters  
 *phti*  
 Pointer to a **LHITTESTINFO** structure containing any information about the link the user clicked.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [LM_HITTEST](http://msdn.microsoft.com/library/windows/desktop/bb760722), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CLinkCtrl Class](../vs140/CLinkCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)