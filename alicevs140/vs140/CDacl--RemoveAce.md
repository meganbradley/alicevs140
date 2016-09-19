---
title: "CDacl::RemoveAce"
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
ms.assetid: 750b6f95-c269-4de6-b233-2058befed0c2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDacl::RemoveAce
Removes a specific ACE (access-control entry) from the `CDacl` object.  
  
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
 [CDacl Class](../vs140/CDacl-Class.md)   
 [CDacl::RemoveAllAces](../vs140/CDacl--RemoveAllAces.md)