---
title: "CAcl::RemoveAce"
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
ms.assetid: 328fe9c6-e231-4b03-82ad-815c3bc65d1a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAcl::RemoveAce
Removes a specific ACE (access-control entry) from the **CAcl** object.  
  
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
 [CAcl Class](../vs140/CAcl-Class.md)   
 [CAcl::RemoveAces](../vs140/CAcl--RemoveAces.md)