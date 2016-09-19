---
title: "CObject::Serialize"
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
ms.assetid: 6e571efe-4947-4e72-a56c-0fe6b552833e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObject::Serialize
Reads or writes this object from or to an archive.  
  
## Syntax  
  
```  
  
      virtual void Serialize(  
   CArchive& ar   
);  
```  
  
#### Parameters  
 `ar`  
 A `CArchive` object to serialize to or from.  
  
## Remarks  
 You must override `Serialize` for each class that you intend to serialize. The overridden `Serialize` must first call the `Serialize` function of its base class.  
  
 You must also use the [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md) macro in your class declaration, and you must use the [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md) macro in the implementation.  
  
 Use [CArchive::IsLoading](../vs140/CArchive--IsLoading.md) or [CArchive::IsStoring](../vs140/CArchive--IsStoring.md) to determine whether the archive is loading or storing.  
  
 `Serialize` is called by [CArchive::ReadObject](../vs140/CArchive--ReadObject.md) and [CArchive::WriteObject](../vs140/CArchive--WriteObject.md). These functions are associated with the `CArchive` insertion operator (**<<**) and extraction operator (**>>**).  
  
 For serialization examples, see the article [Serialization: Serializing an Object](../vs140/Serialization--Serializing-an-Object.md).  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all `CObject` examples.  
  
 [!CODE [NVC_MFCCObjectSample#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#13)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CObject Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)