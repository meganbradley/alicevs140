---
title: "AtlComQIPtrAssign"
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
ms.assetid: eab94dad-65e1-47c8-8ba8-edce86b2760f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlComQIPtrAssign
Assigns an interface pointer to another interface pointer of a different type.  
  
## Syntax  
  
```  
  
      ATLINLINE ATLAPI_(IUnknown*) AtlComQIPtrAssign(  
   IUnknown** pp,  
   IUnknown* lp,  
   REFIID riid  
);  
```  
  
#### Parameters  
 `pp`  
 Address of an **IUnknown** pointer to which to assign another pointer.  
  
 `lp`  
 An **IUnknown** pointer of a type different from the one in `pp`. This is assigned to the pointer in `pp`.  
  
 `riid`  
 The IID of the requested interface.  
  
## Return Value  
 Returns NULL on error; otherwise returns `lp`.  
  
## Remarks  
 This function copies an interface pointer using COM reference counting rules. It calls `QueryInterface` on `lp`, specifying `riid` to obtain the required interface. It calls **Release** on the interface pointed to by `pp` and then assigns the pointer returned by `QueryInterface`.  
  
 This smart pointer helper function is used by [CComPtr Class](../vs140/CComPtr-Class.md) and [CComQIPtr Class](../vs140/CComQIPtr-Class.md).  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtr Class](../vs140/CComPtr-Class.md)   
 [CComQIPtr Class](../vs140/CComQIPtr-Class.md)