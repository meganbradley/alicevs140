---
title: "COleControlSite::DestroyControl"
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
ms.assetid: 98164bb1-b779-44ed-be34-035fd1bacfa2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::DestroyControl
Destroys the `COleControlSite` object.  
  
## Syntax  
  
```  
  
virtual BOOL DestroyControl( );  
  
```  
  
## Return Value  
 Nonzero if successful, otherwise 0.  
  
## Remarks  
 Once completed, the object is freed from memory and any pointers to the object are no longer valid.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)