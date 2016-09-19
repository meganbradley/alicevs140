---
title: "WeakRef::WeakRef Constructor"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 589f87e0-8dcc-4e82-aab2-f2f66f1ec47c
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WeakRef::WeakRef Constructor
Initializes a new instance of the WeakRef class.  
  
## Syntax  
  
```  
WeakRef();  
WeakRef(  
   decltype(__nullptr)  
);  
  
WeakRef(  
   _In_opt_ IWeakReference* ptr  
);  
  
WeakRef(  
   const ComPtr<IWeakReference>& ptr  
);  
  
WeakRef(  
   const WeakRef& ptr  
);  
  
WeakRef(  
   _Inout_ WeakRef&& ptr  
);  
```  
  
#### Parameters  
 `ptr`  
 A pointer, reference, or rvalue-reference to an existing object that initializes the current WeakRef object.  
  
## Remarks  
 The first constructor initializes an empty WeakRef object. The second constructor initializes a WeakRef object from a pointer to the IWeakReference interface. The third constructor initializes a WeakRef object from a reference to a ComPtr< IWeakReference> object. The fourth and fifth constructors initializes a WeakRef object from another WeakRef object.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [WeakRef Class](../vs140/WeakRef-Class.md)