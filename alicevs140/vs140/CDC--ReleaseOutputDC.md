---
title: "CDC::ReleaseOutputDC"
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
ms.assetid: a646b79c-097a-4363-8e27-e6d0e88dfb7e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::ReleaseOutputDC
Call this member function to set the `m_hDC` member to **NULL**.  
  
## Syntax  
  
```  
  
virtual void ReleaseOutputDC( );  
```  
  
## Remarks  
 This member function cannot be called when the output device context is attached to the `CDC` object. Use the **Detach** member function to detach the output device context.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetAttribDC](../vs140/CDC--SetAttribDC.md)   
 [CDC::SetOutputDC](../vs140/CDC--SetOutputDC.md)   
 [CDC::ReleaseAttribDC](../vs140/CDC--ReleaseAttribDC.md)   
 [CDC::m_hDC](../vs140/CDC--m_hDC.md)