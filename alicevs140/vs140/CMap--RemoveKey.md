---
title: "CMap::RemoveKey"
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
ms.assetid: e18362f0-28de-4ab1-bf52-9039e6cbdb68
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::RemoveKey
Looks up the map entry corresponding to the supplied key; then, if the key is found, removes the entry.  
  
## Syntax  
  
```  
  
      BOOL RemoveKey(  
   ARG_KEY key   
);  
```  
  
#### Parameters  
 `ARG_KEY`  
 Template parameter specifying the type of the key.  
  
 `key`  
 Key for the element to be removed.  
  
## Return Value  
 Nonzero if the entry was found and successfully removed; otherwise 0.  
  
## Remarks  
 The **DestructElements** helper function is used to remove the entry.  
  
## Example  
 See the example for [CMap::SetAt](../vs140/CMap--SetAt.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMap::RemoveAll](../vs140/CMap--RemoveAll.md)