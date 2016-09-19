---
title: "CAtlList::RemoveAll"
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
ms.assetid: f407d446-704c-4943-b5b4-7be57ea85f4d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlList::RemoveAll
Call this method to remove all of the elements from the list.  
  
## Syntax  
  
```  
  
void RemoveAll( ) throw( );  
  
```  
  
## Remarks  
 This method removes all of the elements from the list and frees the allocated memory. In debugs builds, an ATLASSERT will be raised if all elements aren't deleted or if the list structure has become corrupted.  
  
## Example  
 See the example for [CAtlList::IsEmpty](../vs140/CAtlList--IsEmpty.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlList Class](../vs140/CAtlList-Class.md)   
 [CAtlList::RemoveAt](../vs140/CAtlList--RemoveAt.md)