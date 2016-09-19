---
title: "CDC::LPtoHIMETRIC"
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
ms.assetid: a015787c-0312-4f9d-a2a3-017c377db1ad
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::LPtoHIMETRIC
Call this function to convert logical units into **HIMETRIC** units.  
  
## Syntax  
  
```  
  
      void LPtoHIMETRIC(   
   LPSIZE lpSize    
) const;  
```  
  
#### Parameters  
 `lpSize`  
 Points to a **SIZE** structure or a `CSize` object.  
  
## Remarks  
 Use this function when you give **HIMETRIC** sizes to OLE, converting from your application's natural mapping mode. Note that the extents of the device's window and viewport will affect the result.  
  
 The conversion is accomplished by first converting the logical units into pixels using the device context's current mapping units and then converting these units into **HIMETRIC** units.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::HIMETRICtoLP](../vs140/CDC--HIMETRICtoLP.md)   
 [CDC::LPtoDP](../vs140/CDC--LPtoDP.md)   
 [CDC::DPtoHIMETRIC](../vs140/CDC--DPtoHIMETRIC.md)