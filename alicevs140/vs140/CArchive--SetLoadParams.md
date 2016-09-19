---
title: "CArchive::SetLoadParams"
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
ms.assetid: a9f604e3-eb2d-4e9d-8d8a-060c01789453
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::SetLoadParams
Call `SetLoadParams` when you are going to read a large number of `CObject`-derived objects from an archive.  
  
## Syntax  
  
```  
  
      void SetLoadParams(  
   UINT nGrowBy = 1024   
);  
```  
  
#### Parameters  
 `nGrowBy`  
 The minimum number of element slots to allocate if a size increase is necessary.  
  
## Remarks  
 `CArchive` uses a load array to resolve references to objects stored in the archive. `SetLoadParams` allows you to set the size to which the load array grows.  
  
 You must not call `SetLoadParams` after any object is loaded, or after [MapObject](../vs140/CArchive--MapObject.md) or [ReadObject](../vs140/CArchive--ReadObject.md) is called.  
  
## Example  
 [!CODE [NVC_MFCSerialization#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#26)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::SetStoreParams](../vs140/CArchive--SetStoreParams.md)