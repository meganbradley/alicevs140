---
title: "CObject::IsKindOf"
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
ms.assetid: 7c87c748-b7e0-4c6d-9694-6035e62fdfd6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObject::IsKindOf
Tests this object's relationship to a given class.  
  
## Syntax  
  
```  
  
      BOOL IsKindOf(  
   const CRuntimeClass* pClass   
) const;  
```  
  
#### Parameters  
 `pClass`  
 A pointer to a [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) structure associated with your `CObject`-derived class.  
  
## Return Value  
 Nonzero if the object corresponds to the class; otherwise 0.  
  
## Remarks  
 This function tests `pClass` to see if (1) it is an object of the specified class or (2) it is an object of a class derived from the specified class. This function works only for classes declared with the [DECLARE_DYNAMIC](../vs140/DECLARE_DYNAMIC.md), [DECLARE_DYNCREATE](../vs140/DECLARE_DYNCREATE.md), or [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md) macro.  
  
 Do not use this function extensively because it defeats the C++ polymorphism feature. Use virtual functions instead.  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all `CObject` examples.  
  
 [!CODE [NVC_MFCCObjectSample#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#11)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CObject Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObject::GetRuntimeClass](../vs140/CObject--GetRuntimeClass.md)   
 [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md)   
 [Accessing Run-Time Class Information](../vs140/Accessing-Run-Time-Class-Information.md)