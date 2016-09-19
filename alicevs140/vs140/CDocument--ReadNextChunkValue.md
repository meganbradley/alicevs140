---
title: "CDocument::ReadNextChunkValue"
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
ms.assetid: 023c6321-32ef-4a33-8331-c54e1518c900
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::ReadNextChunkValue
Reads the next chunk value.  
  
## Syntax  
  
```  
virtual BOOL ReadNextChunkValue(  
   IFilterChunkValue** ppValue  
);  
```  
  
#### Parameters  
 `ppValue`  
 [out] When the function returns, `ppValue` contains the value that was read.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)