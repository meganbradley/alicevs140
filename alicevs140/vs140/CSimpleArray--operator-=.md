---
title: "CSimpleArray::operator ="
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
ms.assetid: 4f7013bd-7ef6-4317-87c3-a9e0d0324123
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleArray::operator =
Assignment operator.  
  
## Syntax  
  
```  
  
      CSimpleArray< T, TEqual >  
& operator =(  
   const CSimpleArray< T, TEqual >& src   
);  
```  
  
#### Parameters  
 *src*  
 The array to copy.  
  
## Return Value  
 Returns a pointer to the updated `CSimpleArray` object.  
  
## Remarks  
 Copies all elements from the `CSimpleArray` object referenced by *src* into the current array object, replacing all existing data.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#90](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#90)]  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleArray Class](../vs140/CSimpleArray-Class.md)