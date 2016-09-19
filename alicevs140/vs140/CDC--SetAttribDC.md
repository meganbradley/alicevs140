---
title: "CDC::SetAttribDC"
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
ms.assetid: df7ed86b-285e-4850-ac89-6e31c8ba644c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetAttribDC
Call this function to set the attribute device context, `m_hAttribDC`.  
  
## Syntax  
  
```  
  
      virtual void SetAttribDC(  
   HDC hDC   
);  
```  
  
#### Parameters  
 `hDC`  
 A Windows device context.  
  
## Remarks  
 This member function does not attach the device context to the `CDC` object. Only the output device context is attached to a `CDC` object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetOutputDC](../vs140/CDC--SetOutputDC.md)   
 [CDC::ReleaseAttribDC](../vs140/CDC--ReleaseAttribDC.md)   
 [CDC::ReleaseOutputDC](../vs140/CDC--ReleaseOutputDC.md)