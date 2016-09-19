---
title: "IMPLEMENT_DYNAMIC"
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
ms.assetid: 8c2eef04-6e71-4512-be7f-9043bd0ed826
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IMPLEMENT_DYNAMIC
Generates the C++ code necessary for a dynamic `CObject`-derived class with run-time access to the class name and position within the hierarchy.  
  
## Syntax  
  
```  
  
IMPLEMENT_DYNAMIC(  
class_name  
,   
base_class_name )  
```  
  
#### Parameters  
 *class_name*  
 The actual name of the class.  
  
 `base_class_name`  
 The name of the base class.  
  
## Remarks  
 Use the `IMPLEMENT_DYNAMIC` macro in a .cpp module, and then link the resulting object code only once.  
  
 For more information, see [CObject Class Topics](../vs140/Using-CObject.md).  
  
## Example  
 [!CODE [NVC_MFCCObjectSample#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#2)]  
  
 [!CODE [NVC_MFCCObjectSample#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#3)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DECLARE_DYNAMIC](../vs140/DECLARE_DYNAMIC.md)   
 [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md)   
 [CObject::IsKindOf](../vs140/CObject--IsKindOf.md)