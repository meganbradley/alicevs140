---
title: "CAtlArray::GetCount"
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
ms.assetid: a8829319-3e0c-4dbb-bdb1-3d7afa3dc809
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::GetCount
Call this method to return the number of elements stored in the array.  
  
## Syntax  
  
```  
  
size_t GetCount( ) const throw( );  
  
```  
  
## Return Value  
 Returns the number of elements stored in the array.  
  
## Remarks  
 As the first element in the array is at position 0, the value returned by `GetCount` is always 1 greater than the largest index.  
  
## Example  
 See the example for [CAtlArray::GetAt](../vs140/CAtlArray--GetAt.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::GetData](../vs140/CAtlArray--GetData.md)