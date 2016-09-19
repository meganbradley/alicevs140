---
title: "CDC::Detach"
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
ms.assetid: 41500f76-6668-4e7b-bfbc-2c6d93f251cf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::Detach
Call this function to detach `m_hDC` (the output device context) from the `CDC` object and set both `m_hDC` and `m_hAttribDC` to **NULL**.  
  
## Syntax  
  
```  
  
HDC Detach( );  
```  
  
## Return Value  
 A Windows device context.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Attach](../vs140/CDC--Attach.md)   
 [CDC::m_hDC](../vs140/CDC--m_hDC.md)   
 [CDC::m_hAttribDC](../vs140/CDC--m_hAttribDC.md)