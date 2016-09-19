---
title: "CArchive::SerializeClass"
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
ms.assetid: 27e534e5-8c0e-4112-8875-b148ea0d0bdd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::SerializeClass
Call this member function when you want to store and load the version information of a base class.  
  
## Syntax  
  
```  
  
      void SerializeClass(  
   const CRuntimeClass* pClassRef   
);  
```  
  
#### Parameters  
 `pClassRef`  
 A pointer to a run-time class object for the base class.  
  
## Remarks  
 `SerializeClass` reads or writes the reference to a class to the `CArchive` object, depending on the direction of the `CArchive`. Use `SerializeClass` in place of [ReadClass](../vs140/CArchive--ReadClass.md) and [WriteClass](../vs140/CArchive--WriteClass.md) as a convenient way to serialize base-class objects; `SerializeClass` requires less code and fewer parameters.  
  
 Like `ReadClass`, `SerializeClass` verifies that the archived class information is compatible with your runtime class. If it is not compatible, `SerializeClass` will throw a [CArchiveException](../vs140/CArchiveException-Class.md).  
  
 Your runtime class must use [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md) and [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md); otherwise, `SerializeClass` will throw a [CNotSupportedException](../vs140/CNotSupportedException-Class.md).  
  
 Use the [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md) macro to retrieve the value for the `pRuntimeClass` parameter. The base class must have used the [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md) macro.  
  
## Example  
 [!CODE [NVC_MFCSerialization#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#25)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::ReadClass](../vs140/CArchive--ReadClass.md)   
 [CArchive::WriteClass](../vs140/CArchive--WriteClass.md)   
 [CArchive::GetObjectSchema](../vs140/CArchive--GetObjectSchema.md)   
 [CArchive::SetObjectSchema](../vs140/CArchive--SetObjectSchema.md)   
 [CArchiveException Class](../vs140/CArchiveException-Class.md)   
 [CNotSupportedException Class](../vs140/CNotSupportedException-Class.md)