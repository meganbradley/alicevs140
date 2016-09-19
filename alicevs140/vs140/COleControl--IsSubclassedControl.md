---
title: "COleControl::IsSubclassedControl"
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
ms.assetid: d7bf7b1e-2aa2-46b0-a8fc-9504c17c9462
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::IsSubclassedControl
Called by the framework to determine if the control subclasses a Windows control.  
  
## Syntax  
  
```  
  
virtual BOOL IsSubclassedControl( );  
  
```  
  
## Return Value  
 Nonzero if the control is subclassed; otherwise 0.  
  
## Remarks  
 You must override this function and return **TRUE** if your OLE control subclasses a Windows control.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)