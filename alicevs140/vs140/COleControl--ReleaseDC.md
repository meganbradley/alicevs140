---
title: "COleControl::ReleaseDC"
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
ms.assetid: 68f39ac5-cb0a-4760-9dac-36a46966b37e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ReleaseDC
Releases the display device context of a container of a windowless control, freeing the device context for use by other applications.  
  
## Syntax  
  
```  
  
      int ReleaseDC(  
   CDC* pDC   
);  
```  
  
#### Parameters  
 `pDC`  
 Identifies the container device context to be released.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The application must call `ReleaseDC` for each call to [GetDC](../vs140/COleControl--GetDC.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetDC](../vs140/COleControl--GetDC.md)