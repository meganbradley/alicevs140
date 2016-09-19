---
title: "CComObjectRootEx::OuterQueryInterface"
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
ms.assetid: a92c6aac-6ea4-40e1-a787-3caa66eb87de
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRootEx::OuterQueryInterface
Retrieves an indirect pointer to the requested interface.  
  
## Syntax  
  
```  
  
      HRESULT OuterQueryInterface(  
   REFIID iid,  
   void** ppvObject   
);  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer specified in `iid`, or **NULL** if the aggregation does not support the interface.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComObjectRootEx::OuterAddRef](../vs140/CComObjectRootEx--OuterAddRef.md)   
 [CComObjectRootEx::OuterRelease](../vs140/CComObjectRootEx--OuterRelease.md)