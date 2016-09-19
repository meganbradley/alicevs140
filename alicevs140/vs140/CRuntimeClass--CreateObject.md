---
title: "CRuntimeClass::CreateObject"
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
ms.assetid: 52d26c4c-59d7-449f-a79d-a9be9c9aa4d1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRuntimeClass::CreateObject
Call this function to dynamically create the specified class during run time.  
  
## Syntax  
  
```  
  
      CObject* CreateObject( );   
static CObject* PASCAL CreateObject(  
   LPCSTR lpszClassName   
);  
static CObject* PASCAL CreateObject(  
   LPCWSTR lpszClassName   
);  
```  
  
#### Parameters  
 `lpszClassName`  
 The familiar name of the class to be created.  
  
## Return Value  
 A pointer to the newly created object, or **NULL** if the class name is not found or there is insufficient memory to create the object.  
  
## Remarks  
 Classes derived from `CObject` can support dynamic creation, which is the ability to create an object of a specified class at run time. Document, view, and frame classes, for example, should support dynamic creation. For more information on dynamic creation and the `CreateObject` member, see [CObject Class](../vs140/Using-CObject.md) and [CObject Class: Specifying Levels of Functionality](../vs140/Specifying-Levels-of-Functionality.md).  
  
## Example  
 See the example for [IsDerivedFrom](../vs140/CRuntimeClass--IsDerivedFrom.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)