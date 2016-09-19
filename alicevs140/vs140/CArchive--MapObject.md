---
title: "CArchive::MapObject"
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
ms.assetid: e314ae56-6fb3-443e-a9db-21b806be98ef
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::MapObject
Call this member function to place objects in the map that are not really serialized to the file, but that are available for subobjects to reference.  
  
## Syntax  
  
```  
  
      void MapObject(  
   const CObject* pOb   
);  
```  
  
#### Parameters  
 `pOb`  
 A constant pointer to the object being stored.  
  
## Remarks  
 For example, you might not serialize a document, but you would serialize the items that are part of the document. By calling `MapObject`, you allow those items, or subobjects, to reference the document. Also, serialized subitems can serialize their `m_pDocument` back pointer.  
  
 You can call `MapObject` when you store to and load from the `CArchive` object. `MapObject` adds the specified object to the internal data structures maintained by the `CArchive` object during serialization and deserialization, but unlike [ReadObject](../vs140/CArchive--ReadObject.md) and [WriteObject](../vs140/CArchive--WriteObject.md)**,** it does not call serialize on the object.  
  
## Example  
 [!CODE [NVC_MFCSerialization#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#18)]  
  
 [!CODE [NVC_MFCSerialization#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#19)]  
  
 [!CODE [NVC_MFCSerialization#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#20)]  
  
 [!CODE [NVC_MFCSerialization#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#21)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::ReadObject](../vs140/CArchive--ReadObject.md)   
 [CArchive::WriteObject](../vs140/CArchive--WriteObject.md)