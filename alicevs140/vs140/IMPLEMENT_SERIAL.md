---
title: "IMPLEMENT_SERIAL"
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
ms.topic: article
ms.assetid: 83dbcfe2-abe4-4fd7-aba1-9a4c1c23f078
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IMPLEMENT_SERIAL
Generates the C++ code necessary for a dynamic `CObject`-derived class with run-time access to the class name and position within the hierarchy.  
  
## Syntax  
  
```  
  
IMPLEMENT_SERIAL(  
class_name  
,   
base_class_name  
,   
wSchema )  
```  
  
#### Parameters  
 *class_name*  
 The actual name of the class.  
  
 `base_class_name`  
 The name of the base class.  
  
 *wSchema*  
 A **UINT** "version number" that will be encoded in the archive to enable a deserializing program to identify and handle data created by earlier program versions. The class schema number must not be –1.  
  
## Remarks  
 Use the `IMPLEMENT_SERIAL` macro in a .cpp module; then link the resulting object code only once.  
  
 You can use the **AFX_API** macro to automatically export the `CArchive` extraction operator for classes that use the `DECLARE_SERIAL` and `IMPLEMENT_SERIAL` macros. Bracket the class declarations (located in the .h file) with the following code:  
  
 [!CODE [NVC_MFCCObjectSample#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#20)]  
  
 For more information, see the [CObject Class Topics](../vs140/Using-CObject.md).  
  
## Example  
 [!CODE [NVC_MFCCObjectSample#24](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#24)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md)   
 [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md)   
 [CObject::IsKindOf](../vs140/CObject--IsKindOf.md)