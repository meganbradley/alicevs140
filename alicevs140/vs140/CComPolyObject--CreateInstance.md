---
title: "CComPolyObject::CreateInstance"
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
ms.assetid: d469a5da-8677-498c-971d-bcf0c956728e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPolyObject::CreateInstance
Allows you to create a new **CComPolyObject<**`contained` **>** object without the overhead of [CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615).  
  
## Syntax  
  
```  
  
      static HRESULT WINAPI CreateInstance(  
   LPUNKNOWN pUnkOuter,   
   CComPolyObject< contained >** pp   
);  
```  
  
#### Parameters  
 `pp`  
 [out] A pointer to a **CComPolyObject<** `contained`**>** pointer. If `CreateInstance` is unsuccessful, `pp` is set to **NULL**.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The object returned has a reference count of zero, so call `AddRef` immediately, then use **Release** to free the reference on the object pointer when you're done.  
  
 If you don't need direct access to the object, but still want to create a new object without the overhead of `CoCreateInstance`, use [CComCoClass::CreateInstance](../vs140/CComCoClass--CreateInstance.md) instead.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComPolyObject Class](../vs140/CComPolyObject-Class.md)