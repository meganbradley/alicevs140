---
title: "RUNTIME_CLASS"
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
ms.assetid: 98cbea2a-a210-44f3-8bc0-0bed990d7014
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RUNTIME_CLASS
Gets the run-time class structure from the name of a C++ class.  
  
## Syntax  
  
```  
  
RUNTIME_CLASS(  
class_name )  
```  
  
#### Parameters  
 *class_name*  
 The actual name of the class (not enclosed in quotation marks).  
  
## Remarks  
 `RUNTIME_CLASS` returns a pointer to a [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) structure for the class specified by *class_name*. Only `CObject`-derived classes declared with `DECLARE_DYNAMIC`, `DECLARE_DYNCREATE`, or `DECLARE_SERIAL` will return pointers to a `CRuntimeClass` structure.  
  
 For more information, see [CObject Class Topics](../vs140/Using-CObject.md).  
  
## Example  
 [!CODE [NVC_MFCCObjectSample#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#25)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DECLARE_DYNAMIC](../vs140/DECLARE_DYNAMIC.md)   
 [DECLARE_DYNCREATE](../vs140/DECLARE_DYNCREATE.md)   
 [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md)   
 [CObject::GetRuntimeClass](../vs140/CObject--GetRuntimeClass.md)   
 [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md)