---
title: "CDC::m_hDC"
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
ms.assetid: 81c10ba5-75be-4bc1-9687-13bbc6fcd0d1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::m_hDC
The output device context for this `CDC` object.  
  
## Syntax  
  
```  
  
HDC m_hDC;  
  
```  
  
## Remarks  
 By default, `m_hDC` is equal to `m_hAttribDC`, the other device context wrapped by `CDC`. In general, `CDC` GDI calls that create output go to the `m_hDC` device context. You can initialize `m_hDC` and `m_hAttribDC` to point to different devices. See the [CDC](../vs140/CDC-Class.md) class description for more on the use of these two device contexts.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::m_hAttribDC](../vs140/CDC--m_hAttribDC.md)   
 [CDC::SetOutputDC](../vs140/CDC--SetOutputDC.md)   
 [CDC::ReleaseOutputDC](../vs140/CDC--ReleaseOutputDC.md)