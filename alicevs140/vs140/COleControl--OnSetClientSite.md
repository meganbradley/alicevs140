---
title: "COleControl::OnSetClientSite"
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
ms.assetid: f7634662-4750-48a5-a52b-02708a68a683
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnSetClientSite
Called by the framework when the container has called the control's **IOleControl::SetClientSite** function.  
  
## Syntax  
  
```  
  
virtual void OnSetClientSite( );  
```  
  
## Remarks  
 By default, `OnSetClientSite` checks whether data path properties are loaded and, if they are, calls `DoDataPathPropExchange`.  
  
 Override this function to do any special processing of this notification. In particular, overrides of this function should call the base class.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)