---
title: "IMPLEMENT_DYNCREATE"
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
ms.assetid: 89ebcfa1-cc4d-49eb-a09b-8618f44f5e98
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IMPLEMENT_DYNCREATE
Enables objects of `CObject`-derived classes to be created dynamically at run time when used with the `DECLARE_DYNCREATE` macro.  
  
## Syntax  
  
```  
  
IMPLEMENT_DYNCREATE(  
class_name, base_class_name )  
```  
  
#### Parameters  
 *class_name*  
 The actual name of the class.  
  
 `base_class_name`  
 The actual name of the base class.  
  
## Remarks  
 The framework uses this ability to create new objects dynamically, for example, when it reads an object from disk during serialization. Add the `IMPLEMENT_DYNCREATE` macro in the class implementation file. For more information, see [CObject Class Topics](../vs140/Using-CObject.md).  
  
 If you use the `DECLARE_DYNCREATE` and `IMPLEMENT_DYNCREATE` macros, you can then use the `RUNTIME_CLASS` macro and the `CObject::IsKindOf` member function to determine the class of your objects at run time.  
  
 If `DECLARE_DYNCREATE` is included in the class declaration, then `IMPLEMENT_DYNCREATE` must be included in the class implementation.  
  
 Note that this macro definition will invoke the default constructor for your class. If a non-trivial constructor is explicitly implemented by the class, it must also explicitly implement the default constructor as well. The default constructor can be added to the class's **private** or **protected** member sections to prevent it from being called from outside the class implementation.  
  
## Example  
 [!CODE [NVC_MFCCObjectSample#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#22)]  
  
 [!CODE [NVC_MFCCObjectSample#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#23)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DECLARE_DYNCREATE](../vs140/DECLARE_DYNCREATE.md)   
 [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md)   
 [CObject::IsKindOf](../vs140/CObject--IsKindOf.md)