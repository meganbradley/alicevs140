---
title: "CDC::HIMETRICtoDP"
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
ms.assetid: 98a71f0e-94a7-4fe4-9cb3-1b18f1c3ac6e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::HIMETRICtoDP
Use this function when you convert **HIMETRIC** sizes from OLE to pixels.  
  
## Syntax  
  
```  
  
      void HIMETRICtoDP(  
   LPSIZE lpSize   
) const;  
```  
  
#### Parameters  
 `lpSize`  
 Points to a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or [CSize](../vs140/CSize-Class.md) object.  
  
## Remarks  
 If the mapping mode of the device context object is `MM_LOENGLISH`, `MM_HIENGLISH`, `MM_LOMETRIC` or `MM_HIMETRIC`, then the conversion is based on the number of pixels in the physical inch. If the mapping mode is one of the other non-constrained modes (e.g., `MM_TEXT`), then the conversion is based on the number of pixels in the logical inch.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::LPtoDP](../vs140/CDC--LPtoDP.md)   
 [CDC::HIMETRICtoLP](../vs140/CDC--HIMETRICtoLP.md)