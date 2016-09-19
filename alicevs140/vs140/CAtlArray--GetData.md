---
title: "CAtlArray::GetData"
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
ms.assetid: c3344ec0-927e-4cb5-9425-38b067061ace
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::GetData
Call this method to return a pointer to the first element in the array.  
  
## Syntax  
  
```  
  
      E* GetData( ) throw( );   
const E* GetData( ) const throw( );  
```  
  
## Return Value  
 Returns a pointer to the memory location storing the first element in the array. If no elements are available, NULL is returned.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#7](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#7)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::GetCount](../vs140/CAtlArray--GetCount.md)