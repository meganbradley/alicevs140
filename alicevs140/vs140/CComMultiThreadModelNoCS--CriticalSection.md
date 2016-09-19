---
title: "CComMultiThreadModelNoCS::CriticalSection"
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
ms.assetid: f82d6324-e1f3-43f9-b684-735f2a378d12
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComMultiThreadModelNoCS::CriticalSection
When using `CComMultiThreadModelNoCS`, the `typedef` name `CriticalSection` references class [CComFakeCriticalSection](../vs140/CComFakeCriticalSection-Class.md).  
  
## Syntax  
  
```  
  
typedef CComFakeCriticalSection CriticalSection;  
  
```  
  
## Remarks  
 Because `CComFakeCriticalSection` does not provide a critical section, its methods do nothing.  
  
 [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md) and [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) also contain definitions for `CriticalSection`. The following table shows the relationship between the threading model class and the critical section class referenced by `CriticalSection`:  
  
|Class defined in|Class referenced|  
|----------------------|----------------------|  
|`CComMultiThreadModelNoCS`|`CComFakeCriticalSection`|  
|`CComMultiThreadModel`|`CComCriticalSection`|  
|`CComSingleThreadModel`|`CComFakeCriticalSection`|  
  
 In addition to `CriticalSection`, you can use the `typedef` name `AutoCriticalSection`. You should not specify `AutoCriticalSection` in global objects or static class members if you want to eliminate the CRT startup code.  
  
## Example  
 See [CComMultiThreadModel::AutoCriticalSection](../vs140/CComMultiThreadModel--AutoCriticalSection.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComMultiThreadModelNoCS Class](../vs140/CComMultiThreadModelNoCS-Class.md)   
 [CComObjectThreadModel](../vs140/CComObjectThreadModel.md)   
 [CComGlobalsThreadModel](../vs140/CComGlobalsThreadModel.md)   
 [CComMultiThreadModelNoCS::ThreadModelNoCS](../vs140/CComMultiThreadModelNoCS--ThreadModelNoCS.md)