---
title: "CArchive::SetStoreParams"
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
ms.assetid: ee710405-01be-4da8-be4d-414494fa327d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::SetStoreParams
Use `SetStoreParams` when storing a large number of `CObject`-derived objects in an archive.  
  
## Syntax  
  
```  
  
      void SetStoreParams(  
   UINT nHashSize = 2053,  
   UINT nBlockSize = 128   
);  
```  
  
#### Parameters  
 *nHashSize*  
 The size of the hash table for interface pointer maps. Should be a prime number.  
  
 `nBlockSize`  
 Specifies the memory-allocation granularity for extending the parameters. Should be a power of 2 for the best performance.  
  
## Remarks  
 `SetStoreParams` allows you to set the hash table size and the block size of the map used to identify unique objects during the serialization process.  
  
 You must not call `SetStoreParams` after any objects are stored, or after [MapObject](../vs140/CArchive--MapObject.md) or [WriteObject](../vs140/CArchive--WriteObject.md) is called.  
  
## Example  
 [!CODE [NVC_MFCSerialization#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#26)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::SetLoadParams](../vs140/CArchive--SetLoadParams.md)