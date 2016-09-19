---
title: "CD2DSizeF::CD2DSizeF"
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
ms.assetid: 74ba5023-466a-46b7-9695-51a69d12ee59
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DSizeF::CD2DSizeF
Constructs a CD2DSizeF object from CSize object.  
  
## Syntax  
  
```  
CD2DSizeF(  
   const CSize& size  
);  
CD2DSizeF(  
   const D2D1_SIZE_F& size  
);  
CD2DSizeF(  
   const D2D1_SIZE_F* size  
);  
CD2DSizeF(  
   FLOAT cx = 0.,  
   FLOAT cy = 0.  
);  
```  
  
#### Parameters  
 `size`  
 source size  
  
 `cx`  
 source width  
  
 `cy`  
 source height  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DSizeF Class](../vs140/CD2DSizeF-Class.md)