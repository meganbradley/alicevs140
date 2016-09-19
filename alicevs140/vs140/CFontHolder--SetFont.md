---
title: "CFontHolder::SetFont"
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
ms.assetid: 632a96d5-9813-4a6c-a263-ba4d68f613f6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFontHolder::SetFont
Releases any existing font and connects the `CFontHolder` object to an `IFont` interface.  
  
## Syntax  
  
```  
  
      void SetFont(  
   LPFONT pNewFont   
);  
```  
  
#### Parameters  
 *pNewFont*  
 Pointer to the new `IFont` interface.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CFontHolder Class](../vs140/CFontHolder-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFontHolder::ReleaseFont](../vs140/CFontHolder--ReleaseFont.md)