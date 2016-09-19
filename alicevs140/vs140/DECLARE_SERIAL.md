---
title: "DECLARE_SERIAL"
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
ms.assetid: 1c1ec454-a666-4743-8ea5-5c059ef2868d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_SERIAL
Generates the C++ header code necessary for a `CObject`-derived class that can be serialized.  
  
## Syntax  
  
```  
  
DECLARE_SERIAL(  
class_name )  
```  
  
#### Parameters  
 *class_name*  
 The actual name of the class.  
  
## Remarks  
 Serialization is the process of writing or reading the contents of an object to and from a file.  
  
 Use the `DECLARE_SERIAL` macro in an .h module, and then include that module in all .cpp modules that need access to objects of this class.  
  
 If `DECLARE_SERIAL` is included in the class declaration, then `IMPLEMENT_SERIAL` must be included in the class implementation.  
  
 The `DECLARE_SERIAL` macro includes all the functionality of `DECLARE_DYNAMIC` and `DECLARE_DYNCREATE`.  
  
 You can use the **AFX_API** macro to automatically export the `CArchive` extraction operator for classes that use the `DECLARE_SERIAL` and `IMPLEMENT_SERIAL` macros. Bracket the class declarations (located in the .h file) with the following code:  
  
 [!CODE [NVC_MFCCObjectSample#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#20)]  
  
 For more information on the `DECLARE_SERIAL` macro, see [CObject Class Topics](../vs140/Using-CObject.md).  
  
## Example  
 [!CODE [NVC_MFCCObjectSample#21](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#21)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DECLARE_DYNAMIC](../vs140/DECLARE_DYNAMIC.md)   
 [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md)   
 [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md)   
 [CObject::IsKindOf](../vs140/CObject--IsKindOf.md)