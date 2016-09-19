---
title: "CStringData::Release"
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
ms.assetid: 1de7a2b6-1d37-4a13-af02-702434355a4f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringData::Release
Decrements the reference count of the string data object.  
  
## Syntax  
  
```  
  
void Release( ) throw( );  
  
```  
  
## Remarks  
 Call this function to decrement the reference count, freeing the `CStringData` structure if the reference count hits zero. This is commonly done when a string object is deleted, and therefore no longer needs to reference the string data object.  
  
 For example, the following code would call `CStringData::Release` for the string data object associated with `str1`:  
  
 [!CODE [NVC_ATLMFC_Utilities#104](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#104)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStringData Class](../vs140/CStringData-Class.md)