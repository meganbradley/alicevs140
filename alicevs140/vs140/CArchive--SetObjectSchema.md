---
title: "CArchive::SetObjectSchema"
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
ms.assetid: 51cb141d-35f4-48ff-89d6-0c1fc5b4d73a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::SetObjectSchema
Call this member function to set the object schema stored in the archive object to `nSchema`.  
  
## Syntax  
  
```  
  
      void SetObjectSchema(  
   UINT nSchema   
);  
```  
  
#### Parameters  
 `nSchema`  
 Specifies the object's schema.  
  
## Remarks  
 The next call to [GetObjectSchema](../vs140/CArchive--GetObjectSchema.md) will return the value stored in `nSchema`.  
  
 Use `SetObjectSchema` for advanced versioning; for example, when you want to force a particular version to be read in a `Serialize` function of a derived class.  
  
## Example  
 [!CODE [NVC_MFCSerialization#27](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#27)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::GetObjectSchema](../vs140/CArchive--GetObjectSchema.md)