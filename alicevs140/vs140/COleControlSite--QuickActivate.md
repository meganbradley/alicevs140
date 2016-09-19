---
title: "COleControlSite::QuickActivate"
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
ms.assetid: 30519635-16d0-4ab5-a582-9f1bf67ebfe1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::QuickActivate
Quick activates the contained control.  
  
## Syntax  
  
```  
  
virtual BOOL QuickActivate( );  
  
```  
  
## Return Value  
 Nonzero if the control site was activated, otherwise zero.  
  
## Remarks  
 This function should be called only if the user is overriding the creation process of the control.  
  
 The `IPersist*::Load` and `IPersist*::InitNew` methods should be called after quick activation occurs. The control should establish its connections to the container's sinks during quick activation. However, these connections are not live until `IPersist*::Load` or `IPersist*::InitNew` has been called.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)