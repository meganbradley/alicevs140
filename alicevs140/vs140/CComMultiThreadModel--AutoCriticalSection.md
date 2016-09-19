---
title: "CComMultiThreadModel::AutoCriticalSection"
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
ms.assetid: 8ebe567d-38eb-4661-9204-d64d8c48d47b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComMultiThreadModel::AutoCriticalSection
When using `CComMultiThreadModel`, the `typedef` name `AutoCriticalSection` references class [CComAutoCriticalSection](../vs140/CComAutoCriticalSection-Class.md), which provides methods for obtaining and releasing ownership of a critical section object.  
  
## Syntax  
  
```  
  
typedef CComAutoCriticalSection AutoCriticalSection;  
  
```  
  
## Remarks  
 [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) and [CComMultiThreadModelNoCS](../vs140/CComMultiThreadModelNoCS-Class.md) also contain definitions for `AutoCriticalSection`. The following table shows the relationship between the threading model class and the critical section class referenced by `AutoCriticalSection`:  
  
|Class defined in|Class referenced|  
|----------------------|----------------------|  
|`CComMultiThreadModel`|`CComCriticalSection`|  
|`CComSingleThreadModel`|`CComFakeCriticalSection`|  
|`CComMultiThreadModelNoCS`|`CComFakeCriticalSection`|  
  
 In addition to `AutoCriticalSection`, you can use the `typedef` name [CriticalSection](../vs140/CComMultiThreadModel--CriticalSection.md). You should not specify `AutoCriticalSection` in global objects or static class members if you want to eliminate the CRT startup code.  
  
## Example  
 The following code is modeled after [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md), and demonstrates `AutoCriticalSection` being used in a threading environment.  
  
 [!CODE [NVC_ATL_COM#36](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#36)]  
  
 The following tables show the results of the `InternalAddRef` and `Lock` methods, depending on the **ThreadModel** template parameter and the threading model used by the application:  
  
### ThreadModel = CComObjectThreadModel  
  
|Method|Single or Apartment Threading|Free Threading|  
|------------|-----------------------------------|--------------------|  
|`InternalAddRef`|The increment is not thread-safe.|The increment is thread-safe.|  
|`Lock`|Does nothing; there is no critical section to lock.|The critical section is locked.|  
  
### ThreadModel = CComObjectThreadModel::ThreadModelNoCS  
  
|Method|Single or Apartment Threading|Free Threading|  
|------------|-----------------------------------|--------------------|  
|`InternalAddRef`|The increment is not thread-safe.|The increment is thread-safe.|  
|`Lock`|Does nothing; there is no critical section to lock.|Does nothing; there is no critical section to lock.|  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComMultiThreadModel Class](../vs140/CComMultiThreadModel-Class.md)   
 [CComObjectThreadModel](../vs140/CComObjectThreadModel.md)   
 [CComGlobalsThreadModel](../vs140/CComGlobalsThreadModel.md)   
 [CComMultiThreadModel::ThreadModelNoCS](../vs140/CComMultiThreadModel--ThreadModelNoCS.md)