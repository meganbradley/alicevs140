---
title: "CObject::CObject"
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
ms.assetid: c0535cab-4bb5-429c-85c5-2e4be0dd793f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObject::CObject
These functions are the standard `CObject` constructors.  
  
## Syntax  
  
```  
  
      CObject( );  
CObject( const CObject& objectSrc );  
```  
  
#### Parameters  
 *objectSrc*  
 A reference to another `CObject`  
  
## Remarks  
 The default version is automatically called by the constructor of your derived class.  
  
 If your class is serializable (it incorporates the `IMPLEMENT_SERIAL` macro), then you must have a default constructor (a constructor with no arguments) in your class declaration. If you do not need a default constructor, declare a private or protected "empty" constructor. For more information, see [Using CObject](../vs140/Using-CObject.md).  
  
 The standard C++ default class copy constructor does a member-by-member copy. The presence of the private `CObject` copy constructor guarantees a compiler error message if the copy constructor of your class is needed but not available. You must therefore provide a copy constructor if your class requires this capability.  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in the `CObject` examples.  
  
 [!CODE [NVC_MFCCObjectSample#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#8)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CObject Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)