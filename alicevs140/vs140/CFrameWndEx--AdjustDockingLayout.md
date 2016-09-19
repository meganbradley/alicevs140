---
title: "CFrameWndEx::AdjustDockingLayout"
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
ms.assetid: 1107bc3d-459f-42cf-abc4-25e9357efb54
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::AdjustDockingLayout
Recalculates the layout of all panes that are docked to the frame window.  
  
## Syntax  
  
```  
virtual void AdjustDockingLayout(  
   HDWP hdwp=NULL   
);  
```  
  
#### Parameters  
 `hdwp`  
 A handle to a structure that contains the positions of multiple windows. .  
  
## Remarks  
 The hdwp structure is initialized by the [BeginDeferWindowPos](http://msdn.microsoft.com/library/windows/desktop/ms632672) method.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)