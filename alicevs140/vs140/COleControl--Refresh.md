---
title: "COleControl::Refresh"
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
ms.assetid: 67603f47-89c5-4d68-9ff9-dcf3f60348f8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::Refresh
Forces a repaint of the OLE control.  
  
## Syntax  
  
```  
  
void Refresh( );  
```  
  
## Remarks  
 This function is supported by the `COleControl` base class as a stock method, called Refresh. This allows users of your OLE control to repaint the control at a specific time. For more information on this method, see the article [ActiveX Controls: Methods](../vs140/MFC-ActiveX-Controls--Methods.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::InvalidateControl](../vs140/COleControl--InvalidateControl.md)