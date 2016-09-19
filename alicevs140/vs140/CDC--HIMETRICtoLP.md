---
title: "CDC::HIMETRICtoLP"
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
ms.assetid: 3d1b132d-1713-4f78-8820-02582715d680
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::HIMETRICtoLP
Call this function to convert **HIMETRIC** units into logical units.  
  
## Syntax  
  
```  
  
      void HIMETRICtoLP(  
   LPSIZE lpSize   
) const;  
```  
  
#### Parameters  
 `lpSize`  
 Points to a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or [CSize](../vs140/CSize-Class.md) object.  
  
## Remarks  
 Use this function when you get **HIMETRIC** sizes from OLE and wish to convert them to your application's natural mapping mode.  
  
 The conversion is accomplished by first converting the **HIMETRIC** units into pixels and then converting these units into logical units using the device context's current mapping units. Note that the extents of the device's window and viewport will affect the result.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::HIMETRICtoDP](../vs140/CDC--HIMETRICtoDP.md)   
 [CDC::DPtoLP](../vs140/CDC--DPtoLP.md)