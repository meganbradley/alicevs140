---
title: "CSacl::RemoveAce"
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
ms.assetid: 23b4ce20-8667-45aa-aeaf-899844d918b1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSacl::RemoveAce
Removes a specific ACE (access-control entry) from the **CSacl** object.  
  
## Syntax  
  
```  
  
      void RemoveAce(   
   UINT nIndex   
) throw( );  
```  
  
#### Parameters  
 `nIndex`  
 Index to the ACE entry to remove.  
  
## Remarks  
 This method is derived from [CAtlArray::RemoveAt](../vs140/CAtlArray--RemoveAt.md).  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSacl Class](../vs140/CSacl-Class.md)   
 [CSacl::RemoveAllAces](../vs140/CSacl--RemoveAllAces.md)