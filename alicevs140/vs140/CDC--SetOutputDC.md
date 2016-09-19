---
title: "CDC::SetOutputDC"
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
ms.assetid: b7600ced-49fb-4ac0-bc4b-9da02f0ee558
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetOutputDC
Call this member function to set the output device context, `m_hDC`.  
  
## Syntax  
  
```  
  
      virtual void SetOutputDC(  
   HDC hDC   
);  
```  
  
#### Parameters  
 `hDC`  
 A Windows device context.  
  
## Remarks  
 This member function can only be called when a device context has not been attached to the `CDC` object. This member function sets `m_hDC` but does not attach the device context to the `CDC` object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetAttribDC](../vs140/CDC--SetAttribDC.md)   
 [CDC::ReleaseAttribDC](../vs140/CDC--ReleaseAttribDC.md)   
 [CDC::ReleaseOutputDC](../vs140/CDC--ReleaseOutputDC.md)   
 [CDC::m_hDC](../vs140/CDC--m_hDC.md)