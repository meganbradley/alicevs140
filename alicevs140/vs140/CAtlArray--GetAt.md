---
title: "CAtlArray::GetAt"
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
ms.assetid: 9e68323e-372b-4556-9f31-4cb072875943
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::GetAt
Call this method to retrieves a single element from the array object.  
  
## Syntax  
  
```  
  
      const E& GetAt(  
   size_t iElement   
) const throw( );  
E& GetAt(  
   size_t iElement   
) throw( );  
```  
  
#### Parameters  
 `iElement`  
 The index value of the array element to return.  
  
## Return Value  
 Returns a reference to the required array element.  
  
## Remarks  
 In debug builds, an ATLASSERT will be raised if `iElement` exceeds the number of elements in the array. In release builds, an invalid argument may lead to unpredictable behavior.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#6](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#6)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::SetAt](../vs140/CAtlArray--SetAt.md)