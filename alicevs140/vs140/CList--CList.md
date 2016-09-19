---
title: "CList::CList"
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
ms.assetid: ffc0df4c-5bb6-4499-a2d3-bab139d7aeff
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::CList
Constructs an empty ordered list.  
  
## Syntax  
  
```  
  
      CList(  
   INT_PTR nBlockSize = 10   
);  
```  
  
#### Parameters  
 `nBlockSize`  
 The memory-allocation granularity for extending the list.  
  
## Remarks  
 As the list grows, memory is allocated in units of `nBlockSize` entries.  
  
## Example  
 [!CODE [NVC_MFCCollections#38](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#38)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)