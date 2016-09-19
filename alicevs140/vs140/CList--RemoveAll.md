---
title: "CList::RemoveAll"
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
ms.assetid: ac41902b-7e5e-4eb9-858a-2b5414f05a0e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CList::RemoveAll
Removes all the elements from this list and frees the associated memory.  
  
## Syntax  
  
```  
  
void RemoveAll( );  
```  
  
## Remarks  
 No error is generated if the list is already empty.  
  
## Example  
 [!CODE [NVC_MFCCollections#51](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#51)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CList Class](../vs140/CList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CList::RemoveAt](../vs140/CList--RemoveAt.md)