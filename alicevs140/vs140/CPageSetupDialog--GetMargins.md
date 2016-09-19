---
title: "CPageSetupDialog::GetMargins"
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
ms.assetid: 68c857ed-f5c3-4807-a223-50635c148e7a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPageSetupDialog::GetMargins
Call this function after a call to `DoModal` to retrieve the margins of the printer device driver.  
  
## Syntax  
  
```  
  
      void GetMargins(  
   LPRECT lpRectMargins,  
   LPRECT lpRectMinMargins   
) const;  
```  
  
#### Parameters  
 *lpRectMargins*  
 Pointer to a [RECT](../vs140/RECT-Structure.md) structure or [CRect](../vs140/CRect-Class.md) object that describes (in 1/1000 inches or 1/100 mm) the print margins for the currently selected printer. Pass **NULL** for this parameter, if you are not interested in this rectangle.  
  
 *lpRectMinMargins*  
 Pointer to a `RECT` structure or `CRect` object that describes (in 1/1000 inches or 1/100 mm) the minimum print margins for the currently selected printer. Pass **NULL** for this parameter, if you are not interested in this rectangle.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPageSetupDialog Class](../vs140/CPageSetupDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)