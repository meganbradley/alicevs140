---
title: "CArchive::WriteClass"
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
ms.assetid: 63bbf65a-51cf-4da3-9e7a-bd5b60d73403
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::WriteClass
Use `WriteClass` to store the version and class information of a base class during serialization of the derived class.  
  
## Syntax  
  
```  
  
      void WriteClass(  
   const CRuntimeClass* pClassRef   
);  
```  
  
#### Parameters  
 `pClassRef`  
 A pointer to the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) structure that corresponds to the class reference requested.  
  
## Remarks  
 `WriteClass` writes a reference to the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) for the base class to the `CArchive`. Use [CArchive::ReadClass](../vs140/CArchive--ReadClass.md) to retrieve the reference.  
  
 `WriteClass` verifies that the archived class information is compatible with your runtime class. If it is not compatible, `WriteClass` will throw a [CArchiveException](../vs140/CArchiveException-Class.md).  
  
 Your runtime class must use [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md) and [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md); otherwise, `WriteClass` will throw a [CNotSupportedException](../vs140/CNotSupportedException-Class.md).  
  
 You can use [SerializeClass](../vs140/CArchive--SerializeClass.md) instead of `WriteClass`, which handles both reading and writing of the class reference.  
  
## Example  
 [!CODE [NVC_MFCSerialization#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#28)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::ReadClass](../vs140/CArchive--ReadClass.md)   
 [CArchive::GetObjectSchema](../vs140/CArchive--GetObjectSchema.md)   
 [CArchive::SetObjectSchema](../vs140/CArchive--SetObjectSchema.md)   
 [CArchive::SerializeClass](../vs140/CArchive--SerializeClass.md)   
 [CArchiveException Class](../vs140/CArchiveException-Class.md)   
 [CNotSupportedException Class](../vs140/CNotSupportedException-Class.md)   
 [CObList::CObList](../vs140/CObList--CObList.md)