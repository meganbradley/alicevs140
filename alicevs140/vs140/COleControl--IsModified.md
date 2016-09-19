---
title: "COleControl::IsModified"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 6d1c701b-21cc-48f2-a172-17903531dfac
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::IsModified
Determines if the control's state has been modified.  
  
## Syntax  
  
```  
  
BOOL IsModified( );  
```  
  
## Return Value  
 Nonzero if the control's state has been modified since it was last saved; otherwise 0.  
  
## Remarks  
 The state of a control is modified when a property changes value.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetModifiedFlag](../vs140/COleControl--SetModifiedFlag.md)