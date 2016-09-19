---
title: "DeferrableEventArgs::GetDeferral Method"
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
ms.assetid: ef6dc7c5-b0be-4b85-8507-d3fd97f2185d
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DeferrableEventArgs::GetDeferral Method
Gets a reference to the [Deferral](http://go.microsoft.com/fwlink/?LinkId=526520) object which represents a deferred event.  
  
## Syntax  
  
```cpp  
HRESULT GetDeferral([out, retval] Windows::Foundation::IDeferral** result)  
```  
  
#### Parameters  
 `result`  
 A pointer that will reference the [Deferral](http://go.microsoft.com/fwlink/?LinkId=526520) object when the call completes.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that indicates the error.  
  
## Remarks  
 For a code example, see [DeferredEventArgs Class](../vs140/DeferrableEventArgs-Class.md).  
  
## Requirements  
 **Header:** event.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [DeferredEventArgs Class](../vs140/DeferrableEventArgs-Class.md)