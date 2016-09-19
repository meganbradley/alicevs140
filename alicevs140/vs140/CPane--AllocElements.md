---
title: "CPane::AllocElements"
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
ms.assetid: 55f52e64-b333-4369-8c09-36e962134f49
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::AllocElements
Allocates storage for internal use.  
  
## Syntax  
  
```  
BOOL AllocElements(  
   int nElements,  
   int cbElement  
);  
```  
  
#### Parameters  
 [in] `nElements`  
 The number of elements for which to allocate storage.  
  
 [in] `cbElement`  
 The size, in bytes, of an element.  
  
## Return Value  
 `FALSE` if memory allocation fails; otherwise, `TRUE`.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)