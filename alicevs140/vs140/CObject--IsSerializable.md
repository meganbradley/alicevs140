---
title: "CObject::IsSerializable"
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
ms.assetid: d8db85a8-4586-4578-97cf-d005370180e8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObject::IsSerializable
Tests whether this object is eligible for serialization.  
  
## Syntax  
  
```  
  
BOOL IsSerializable( ) const;  
```  
  
## Return Value  
 Nonzero if this object can be serialized; otherwise 0.  
  
## Remarks  
 For a class to be serializable, its declaration must contain the [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md) macro, and the implementation must contain the [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md) macro.  
  
> [!NOTE]
>  Do not override this function.  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all `CObject` examples.  
  
 [!CODE [NVC_MFCCObjectSample#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#12)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CObject Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)