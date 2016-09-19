---
title: "WeakReference::Resolve Method"
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
ms.assetid: fc65a4b7-48a0-4d64-a793-37f566fdd8e7
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WeakReference::Resolve Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
  
STDMETHOD(Resolve)  
   (REFIID riid,   
   _Deref_out_opt_ IInspectable **ppvObject  
);  
```  
  
#### Parameters  
 `riid`  
 An interface ID.  
  
 `ppvObject`  
 When this operation completes,  a copy of the current strong reference if the strong reference count is nonzero.  
  
## Return Value  
  
-   S_OK if this operation is successful and the strong reference count is zero. The `ppvObject` parameter is set to `nullptr`.  
  
-   S_OK if this operation is successful and the strong reference count is nonzero. The `ppvObject` parameter is set to the strong reference.  
  
-   Otherwise, an HRESULT that indicates the reason this operation failed.  
  
## Remarks  
 Sets the specified pointer to the current strong reference value if the strong reference count is nonzero.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [WeakReference Class](../vs140/WeakReference-Class.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)