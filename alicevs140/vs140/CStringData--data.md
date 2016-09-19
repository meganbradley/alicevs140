---
title: "CStringData::data"
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
ms.assetid: 641cd096-ef6a-4f11-befe-c223f4ff157a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringData::data
Returns a pointer to the character buffer of a string object.  
  
## Syntax  
  
```  
  
void* data( ) throw( );  
  
```  
  
## Return Value  
 A pointer to the character buffer of the string object.  
  
## Remarks  
 Call this function to return the current character buffer of the associated string object.  
  
> [!NOTE]
>  This buffer is not allocated by the `CStringData` object but by the string manager when needed. When allocated, the buffer is appended to the string data object.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStringData Class](../vs140/CStringData-Class.md)