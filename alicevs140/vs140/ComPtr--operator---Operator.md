---
title: "ComPtr::operator-&gt; Operator"
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
ms.assetid: 7b7faefd-d1e4-4f31-a77d-17a42e0d6b6a
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ComPtr::operator-&gt; Operator
Retrieves a pointer to the type specified by the current template parameter.  
  
## Syntax  
  
```  
WRL_NOTHROW Microsoft::WRL::Details::RemoveIUnknown<InterfaceType>* operator->() const;  
```  
  
## Return Value  
 Pointer to the type specified by the current template type name.  
  
## Remarks  
 This helper function removes unnecessary overhead caused by using the STDMETHOD macro. This function makes IUnknown types private instead of virtual.  
  
## Requirements  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [ComPtr Class](../vs140/ComPtr-Class.md)