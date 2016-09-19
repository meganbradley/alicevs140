---
title: "CDC::ReleaseAttribDC"
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
ms.assetid: ae0ad0d0-505e-4e0f-a535-a3fa3ce5bbc7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::ReleaseAttribDC
Call this member function to set `m_hAttribDC` to **NULL**.  
  
## Syntax  
  
```  
  
virtual void ReleaseAttribDC( );  
```  
  
## Remarks  
 This does not cause a **Detach** to occur. Only the output device context is attached to the `CDC` object, and only it can be detached.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetOutputDC](../vs140/CDC--SetOutputDC.md)   
 [CDC::SetAttribDC](../vs140/CDC--SetAttribDC.md)   
 [CDC::ReleaseOutputDC](../vs140/CDC--ReleaseOutputDC.md)   
 [CDC::m_hAttribDC](../vs140/CDC--m_hAttribDC.md)