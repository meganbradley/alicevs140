---
title: "CDC::SaveDC"
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
ms.assetid: 93d6913a-adcb-4481-9a6f-f2697abf1ec6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SaveDC
Saves the current state of the device context by copying state information (such as clipping region, selected objects, and mapping mode) to a context stack maintained by Windows.  
  
## Syntax  
  
```  
  
virtual int SaveDC( );  
```  
  
## Return Value  
 An integer identifying the saved device context. It is 0 if an error occurs. This return value can be used to restore the device context by calling `RestoreDC`.  
  
## Remarks  
 The saved device context can later be restored by using `RestoreDC`.  
  
 `SaveDC` can be used any number of times to save any number of device-context states.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::RestoreDC](../vs140/CDC--RestoreDC.md)   
 [SaveDC](http://msdn.microsoft.com/library/windows/desktop/dd162945)