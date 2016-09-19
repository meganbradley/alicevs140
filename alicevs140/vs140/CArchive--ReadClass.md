---
title: "CArchive::ReadClass"
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
ms.assetid: 9ebd026f-086d-4aa4-82b0-b201e0b03246
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::ReadClass
Call this member function to read a reference to a class previously stored with [WriteClass](../vs140/CArchive--WriteClass.md).  
  
## Syntax  
  
```  
  
      CRuntimeClass* ReadClass(   
   const CRuntimeClass* pClassRefRequested = NULL,   
   UINT* pSchema = NULL,   
   DWORD* pObTag = NULL    
);  
```  
  
#### Parameters  
 `pClassRefRequested`  
 A pointer to the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) structure that corresponds to the class reference requested. Can be **NULL**.  
  
 `pSchema`  
 A pointer to a schema of the run-time class previously stored.  
  
 `pObTag`  
 A number that refers to an object's unique tag. Used internally by the implementation of [ReadObject](../vs140/CArchive--ReadObject.md). Exposed for advanced programming only; `pObTag` normally should be **NULL**.  
  
## Return Value  
 A pointer to the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) structure.  
  
## Remarks  
 If `pClassRefRequested` is not **NULL**, `ReadClass` verifies that the archived class information is compatible with your runtime class. If it is not compatible, `ReadClass` will throw a [CArchiveException](../vs140/CArchiveException-Class.md).  
  
 Your runtime class must use [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md) and [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md); otherwise, `ReadClass` will throw a [CNotSupportedException](../vs140/CNotSupportedException-Class.md).  
  
 If `pSchema` is **NULL**, the schema of the stored class can be retrieved by calling [CArchive::GetObjectSchema](../vs140/CArchive--GetObjectSchema.md); otherwise, **\***`pSchema` will contain the schema of the run-time class that was previously stored.  
  
 You can use [SerializeClass](../vs140/CArchive--SerializeClass.md) instead of `ReadClass`, which handles both reading and writing of the class reference.  
  
## Example  
 See the example for [CArchive::WriteClass](../vs140/CArchive--WriteClass.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::WriteClass](../vs140/CArchive--WriteClass.md)   
 [CArchive::GetObjectSchema](../vs140/CArchive--GetObjectSchema.md)   
 [CArchive::SetObjectSchema](../vs140/CArchive--SetObjectSchema.md)   
 [CArchiveException Class](../vs140/CArchiveException-Class.md)   
 [CNotSupportedException Class](../vs140/CNotSupportedException-Class.md)   
 [CArchive::SerializeClass](../vs140/CArchive--SerializeClass.md)