---
title: "CAtlArray::IsEmpty"
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
ms.assetid: 5d7e07a5-7a35-4b97-ad99-6735068d4d15
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::IsEmpty
Call this method to test if the array is empty.  
  
## Syntax  
  
```  
  
bool IsEmpty( ) const throw( );  
  
```  
  
## Return Value  
 Returns true if the array is empty, false otherwise.  
  
## Remarks  
 The array is said to be empty if it contains no elements. Therefore, even if the array contains empty elements, it is not empty.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#10](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#10)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::AssertValid](../vs140/CAtlArray--AssertValid.md)