---
title: "CRgn::FromHandle"
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
ms.assetid: 391d75e8-f314-47e1-86d3-82f61e9331e3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::FromHandle
Returns a pointer to a `CRgn` object when given a handle to a Windows region.  
  
## Syntax  
  
```  
  
      static CRgn* PASCAL FromHandle(  
   HRGN hRgn   
);  
```  
  
#### Parameters  
 `hRgn`  
 Specifies a handle to a Windows region.  
  
## Return Value  
 A pointer to a `CRgn` object. If the function was not successful, the return value is **NULL**.  
  
## Remarks  
 If a `CRgn` object is not already attached to the handle, a temporary `CRgn` object is created and attached. This temporary `CRgn` object is valid only until the next time the application has idle time in its event loop, at which time all temporary graphic objects are deleted. Another way of saying this is that the temporary object is only valid during the processing of one window message.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)