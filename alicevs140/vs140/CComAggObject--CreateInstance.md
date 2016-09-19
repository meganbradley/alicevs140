---
title: "CComAggObject::CreateInstance"
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
ms.assetid: fd838b8c-0980-48e3-8b3a-1e94bedf435a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAggObject::CreateInstance
This static function allows you to create a new **CComAggObject<**`contained` **>** object without the overhead of [CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615).  
  
## Syntax  
  
```  
  
      static HRESULT WINAPI CreateInstance(  
   LPUNKNOWN pUnkOuter,   
   CComAggObject< contained >** pp   
);  
```  
  
#### Parameters  
 `pp`  
 [out] A pointer to a **CComAggObject<***contained* **>** pointer. If `CreateInstance` is unsuccessful, `pp` is set to **NULL**.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The object returned has a reference count of zero, so call `AddRef` immediately, then use **Release** to free the reference on the object pointer when you're done.  
  
 If you do not need direct access to the object, but still want to create a new object without the overhead of `CoCreateInstance`, use [CComCoClass::CreateInstance](../vs140/CComCoClass--CreateInstance.md) instead.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComAggObject Class](../vs140/CComAggObject-Class.md)