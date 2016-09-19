---
title: "CComObject::CreateInstance"
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
ms.assetid: cad8ff04-094a-4471-9526-f7286f4c1d85
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObject::CreateInstance
This static function allows you to create a new **CComObject<**`Base`**>** object, without the overhead of [CoCreateInstance](http://msdn.microsoft.com/library/windows/desktop/ms686615).  
  
## Syntax  
  
```  
  
      static HRESULT WINAPI CreateInstance(  
   CComObject< Base >** pp   
);  
```  
  
#### Parameters  
 `pp`  
 [out] A pointer to a **CComObject<**`Base`**>** pointer. If `CreateInstance` is unsuccessful, `pp` is set to **NULL**.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The object returned has a reference count of zero, so call `AddRef` immediately, then use **Release** to free the reference on the object pointer when you're done.  
  
 If you do not need direct access to the object, but still want to create a new object without the overhead of `CoCreateInstance`, use [CComCoClass::CreateInstance](../vs140/CComCoClass--CreateInstance.md) instead.  
  
## Example  
 [!CODE [NVC_ATL_COM#38](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#38)]  
  
 [!CODE [NVC_ATL_COM#39](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#39)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObject Class](../vs140/CComObject-Class.md)