---
title: "CRgn::CreateFromPath"
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
ms.assetid: de893506-3dd9-4de0-a512-8ccf02e975b8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRgn::CreateFromPath
Creates a region from the path that is selected into the given device context.  
  
## Syntax  
  
```  
  
      BOOL CreateFromPath(  
   CDC* pDC   
);  
```  
  
#### Parameters  
 `pDC`  
 Identifies a device context that contains a closed path.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The device context identified by the `pDC` parameter must contain a closed path. After `CreateFromPath` converts a path into a region, Windows discards the closed path from the device context.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CRgn Class](../vs140/CRgn-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::BeginPath](../vs140/CDC--BeginPath.md)   
 [CDC::EndPath](../vs140/CDC--EndPath.md)   
 [CDC::SetPolyFillMode](../vs140/CDC--SetPolyFillMode.md)