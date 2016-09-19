---
title: "CAtlArray::AssertValid"
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
ms.assetid: 77749fcf-85c8-4abf-826d-e9dff30b5d12
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::AssertValid
Call this method to confirm that the array object is valid.  
  
## Syntax  
  
```  
  
void AssertValid( ) const;  
  
```  
  
## Remarks  
 If the array object is not valid, `ATLASSERT` will throw an assertion. This method is available only if _DEBUG is defined.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#3](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#3)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::IsEmpty](../vs140/CAtlArray--IsEmpty.md)