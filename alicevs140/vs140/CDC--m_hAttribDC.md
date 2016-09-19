---
title: "CDC::m_hAttribDC"
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
ms.assetid: 00bdf972-da70-4f01-aaa0-b94a8b1e477f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::m_hAttribDC
The attribute device context for this `CDC` object.  
  
## Syntax  
  
```  
  
HDC m_hAttribDC;  
  
```  
  
## Remarks  
 By default, this device context is equal to `m_hDC`. In general, `CDC` GDI calls that request information from the device context are directed to `m_hAttribDC`. See the [CDC](../vs140/CDC-Class.md) class description for more on the use of these two device contexts.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::m_hDC](../vs140/CDC--m_hDC.md)   
 [CDC::SetAttribDC](../vs140/CDC--SetAttribDC.md)   
 [CDC::ReleaseAttribDC](../vs140/CDC--ReleaseAttribDC.md)