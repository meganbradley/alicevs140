---
title: "CDC::Attach"
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
ms.assetid: a5791015-82f0-4f6a-859e-231e7f0c0e06
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::Attach
Use this member function to attach an `hDC` to the `CDC` object.  
  
## Syntax  
  
```  
  
      BOOL Attach(  
   HDC hDC   
);  
```  
  
#### Parameters  
 `hDC`  
 A Windows device context.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The `hDC` is stored in both `m_hDC`, the output device context, and in `m_hAttribDC`, the attribute device context.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Detach](../vs140/CDC--Detach.md)   
 [CDC::m_hDC](../vs140/CDC--m_hDC.md)   
 [CDC::m_hAttribDC](../vs140/CDC--m_hAttribDC.md)