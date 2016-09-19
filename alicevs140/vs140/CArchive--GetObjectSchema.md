---
title: "CArchive::GetObjectSchema"
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
ms.assetid: 8546decb-5fcf-4f41-b3f1-68e25b9df7ef
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::GetObjectSchema
Call this function from the `Serialize` function to determine the version of the object that is currently being deserialized.  
  
## Syntax  
  
```  
  
UINT GetObjectSchema( );  
```  
  
## Return Value  
 During deserialization, the version of the object being read.  
  
## Remarks  
 Calling this function is only valid when the `CArchive` object is being loaded ([CArchive::IsLoading](../vs140/CArchive--IsLoading.md) returns nonzero). It should be the first call in the `Serialize` function and called only once. A return value of (**UINT**)–1 indicates that the version number is unknown.  
  
 A `CObject`-derived class may use **VERSIONABLE_SCHEMA** combined (using bitwise `OR`) with the schema version itself (in the `IMPLEMENT_SERIAL` macro) to create a "versionable object," that is, an object whose `Serialize` member function can read multiple versions. The default framework functionality (without **VERSIONABLE_SCHEMA**) is to throw an exception when the version is mismatched.  
  
## Example  
 [!CODE [NVC_MFCSerialization#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#15)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)   
 [CObject::IsSerializable](../vs140/CObject--IsSerializable.md)   
 [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md)   
 [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md)   
 [CArchive::IsLoading](../vs140/CArchive--IsLoading.md)