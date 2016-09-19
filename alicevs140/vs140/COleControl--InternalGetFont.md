---
title: "COleControl::InternalGetFont"
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
ms.assetid: 521a644d-3ea7-4a63-bde2-2fd1cf663d27
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::InternalGetFont
Accesses the stock Font property of your control  
  
## Syntax  
  
```  
  
CFontHolder& InternalGetFont( );  
```  
  
## Return Value  
 A reference to a [CFontHolder](../vs140/CFontHolder-Class.md) object that contains the stock Font object.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetFont](../vs140/COleControl--GetFont.md)   
 [COleControl::SetFont](../vs140/COleControl--SetFont.md)