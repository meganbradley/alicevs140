---
title: "STATIC_DOWNCAST"
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
ms.assetid: bcc4471e-2e40-4803-8083-b46e95c74be6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# STATIC_DOWNCAST
Casts *pobject* to a pointer to a *class_name* object.  
  
## Syntax  
  
```  
  
STATIC_DOWNCAST(  
class_name  
, pobject )  
```  
  
#### Parameters  
 *class_name*  
 The name of the class being cast to.  
  
 *pobject*  
 The pointer to be cast to a pointer to a *class_name* object.  
  
## Remarks  
 *pobject* must either be **NULL**, or point to an object of a class which is derived directly, or indirectly, from *class_name*. In builds of your application with the **_DEBUG** preprocessor symbol defined, the macro will **ASSERT** if *pobject* is not **NULL**, or if it points to an object that is not a "kind of" the class specified in the *class_name* parameter (see [CObject::IsKindOf](../vs140/CObject--IsKindOf.md)). In non-**_DEBUG** builds, the macro performs the cast without any type checking.  
  
 The class specified in the *class_name* parameter must be derived from `CObject` and must use the `DECLARE_DYNAMIC` and `IMPLEMENT_DYNAMIC`, the `DECLARE_DYNCREATE` and `IMPLEMENT_DYNCREATE`, or the `DECLARE_SERIAL` and `IMPLEMENT_SERIAL` macros as explained in the article [CObject Class: Deriving a Class from CObject](../vs140/Deriving-a-Class-from-CObject.md).  
  
 For example, you might cast a pointer to `CMyDoc`, called `pMyDoc`, to a pointer to **CDocument** using this expression:  
  
 [!CODE [NVC_MFCDocView#197](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#197)]  
  
 If `pMyDoc` does not point to an object derived directly or indirectly from **CDocument**, the macro will **ASSERT**.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DYNAMIC_DOWNCAST](../vs140/DYNAMIC_DOWNCAST.md)   
 [static_cast Operator](../vs140/static_cast-Operator.md)