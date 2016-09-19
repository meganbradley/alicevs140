---
title: "CComMultiThreadModel::CriticalSection"
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
ms.assetid: ecf6edcb-a1cd-4054-800c-5f2614e9b9f3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComMultiThreadModel::CriticalSection
When using `CComMultiThreadModel`, the `typedef` name `CriticalSection` references class [CComCriticalSection](../vs140/CComCriticalSection-Class.md), which provides methods for obtaining and releasing ownership of a critical section object.  
  
## Syntax  
  
```  
  
typedef CComCriticalSection CriticalSection;  
  
```  
  
## Remarks  
 [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) and [CComMultiThreadModelNoCS](../vs140/CComMultiThreadModelNoCS-Class.md) also contain definitions for `CriticalSection`. The following table shows the relationship between the threading model class and the critical section class referenced by `CriticalSection`:  
  
|Class defined in|Class referenced|  
|----------------------|----------------------|  
|`CComMultiThreadModel`|`CComCriticalSection`|  
|`CComSingleThreadModel`|`CComFakeCriticalSection`|  
|`CComMultiThreadModelNoCS`|`CComFakeCriticalSection`|  
  
 In addition to `CriticalSection`, you can use the `typedef` name [AutoCriticalSection](../vs140/CComMultiThreadModel--AutoCriticalSection.md). You should not specify `AutoCriticalSection` in global objects or static class members if you want to eliminate the CRT startup code.  
  
## Example  
 See [CComMultiThreadModel::AutoCriticalSection](../vs140/CComMultiThreadModel--AutoCriticalSection.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComMultiThreadModel Class](../vs140/CComMultiThreadModel-Class.md)   
 [CComObjectThreadModel](../vs140/CComObjectThreadModel.md)   
 [CComGlobalsThreadModel](../vs140/CComGlobalsThreadModel.md)   
 [CComMultiThreadModel::ThreadModelNoCS](../vs140/CComMultiThreadModel--ThreadModelNoCS.md)