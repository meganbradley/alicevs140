---
title: "CComMultiThreadModelNoCS Class"
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
ms.assetid: 2b3f7a45-fd72-452c-aaf3-ccdaa621c821
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComMultiThreadModelNoCS Class
`CComMultiThreadModelNoCS` provides thread-safe methods for incrementing and decrementing the value of a variable, without critical section locking or unlocking functionality.  
  
## Syntax  
  
```  
  
class CComMultiThreadModelNoCS  
  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CComMultiThreadModelNoCS::AutoCriticalSection](../vs140/CComMultiThreadModelNoCS--AutoCriticalSection.md)|References class [CComFakeCriticalSection](../vs140/CComFakeCriticalSection-Class.md).|  
|[CComMultiThreadModelNoCS::CriticalSection](../vs140/CComMultiThreadModelNoCS--CriticalSection.md)|References class `CComFakeCriticalSection`.|  
|[CComMultiThreadModelNoCS::ThreadModelNoCS](../vs140/CComMultiThreadModelNoCS--ThreadModelNoCS.md)|References class `CComMultiThreadModelNoCS`.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComMultiThreadModelNoCS::Decrement](../vs140/CComMultiThreadModelNoCS--Decrement.md)|(Static) Decrements the value of the specified variable in a thread-safe manner.|  
|[CComMultiThreadModelNoCS::Increment](../vs140/CComMultiThreadModelNoCS--Increment.md)|(Static) Increments the value of the specified variable in a thread-safe manner.|  
  
## Remarks  
 `CComMultiThreadModelNoCS` is similar to [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md) in that it provides thread-safe methods for incrementing and decrementing a variable. However, when you reference a critical section class through `CComMultiThreadModelNoCS`, methods such as `Lock` and `Unlock` will do nothing.  
  
 Typically, you use `CComMultiThreadModelNoCS` through the `ThreadModelNoCS``typedef` name. This `typedef` is defined in `CComMultiThreadModelNoCS`, `CComMultiThreadModel`, and [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md).  
  
> [!NOTE]
>  The global `typedef` names [CComObjectThreadModel](../vs140/CComObjectThreadModel.md) and [CComGlobalsThreadModel](../vs140/CComGlobalsThreadModel.md) do not reference `CComMultiThreadModelNoCS`.  
  
 In addition to `ThreadModelNoCS`, `CComMultiThreadModelNoCS` defines `AutoCriticalSection` and `CriticalSection`. These latter two `typedef` names reference [CComFakeCriticalSection](../vs140/CComFakeCriticalSection-Class.md), which provides empty methods associated with obtaining and releasing a critical section.  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="ccommultithreadmodelnocs__autocriticalsection"></a>  CComMultiThreadModelNoCS::AutoCriticalSection  
 When using `CComMultiThreadModelNoCS`, the `typedef` name `AutoCriticalSection` references class [CComFakeCriticalSection](../vs140/CComFakeCriticalSection-Class.md).  
  
```  
  
typedef CComFakeCriticalSection AutoCriticalSection;  
  
```  
  
### Remarks  
 Because `CComFakeCriticalSection` does not provide a critical section, its methods do nothing.  
  
 [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md) and [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) also contain definitions for `AutoCriticalSection`. The following table shows the relationship between the threading model class and the critical section class referenced by `AutoCriticalSection`:  
  
|Class defined in|Class referenced|  
|----------------------|----------------------|  
|`CComMultiThreadModelNoCS`|`CComFakeCriticalSection`|  
|`CComMultiThreadModel`|`CComAutoCriticalSection`|  
|`CComSingleThreadModel`|`CComFakeCriticalSection`|  
  
 In addition to `AutoCriticalSection`, you can use the `typedef` name [CriticalSection](../vs140/CComMultiThreadModelNoCS--CriticalSection.md). You should not specify `AutoCriticalSection` in global objects or static class members if you want to eliminate the CRT startup code.  
  
### Example  
 See [CComMultiThreadModel::AutoCriticalSection](../vs140/CComMultiThreadModel--AutoCriticalSection.md).  
  
##  <a name="ccommultithreadmodelnocs__criticalsection"></a>  CComMultiThreadModelNoCS::CriticalSection  
 When using `CComMultiThreadModelNoCS`, the `typedef` name `CriticalSection` references class [CComFakeCriticalSection](../vs140/CComFakeCriticalSection-Class.md).  
  
```  
  
typedef CComFakeCriticalSection CriticalSection;  
  
```  
  
### Remarks  
 Because `CComFakeCriticalSection` does not provide a critical section, its methods do nothing.  
  
 [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md) and [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) also contain definitions for `CriticalSection`. The following table shows the relationship between the threading model class and the critical section class referenced by `CriticalSection`:  
  
|Class defined in|Class referenced|  
|----------------------|----------------------|  
|`CComMultiThreadModelNoCS`|`CComFakeCriticalSection`|  
|`CComMultiThreadModel`|`CComCriticalSection`|  
|`CComSingleThreadModel`|`CComFakeCriticalSection`|  
  
 In addition to `CriticalSection`, you can use the `typedef` name `AutoCriticalSection`. You should not specify `AutoCriticalSection` in global objects or static class members if you want to eliminate the CRT startup code.  
  
### Example  
 See [CComMultiThreadModel::AutoCriticalSection](../vs140/CComMultiThreadModel--AutoCriticalSection.md).  
  
##  <a name="ccommultithreadmodelnocs__decrement"></a>  CComMultiThreadModelNoCS::Decrement  
 This static function calls the Win32 function [InterlockedDecrement](http://msdn.microsoft.com/library/windows/desktop/ms683580), which decrements the value of the variable pointed to by `p`.  
  
```  
  
static ULONG WINAPI Decrement(  
      LPLONG  p  
   ) throw( );  
  
```  
  
### Parameters  
 `p`  
 [in] Pointer to the variable to be decremented.  
  
### Return Value  
 If the result of the decrement is 0, then `Decrement` returns 0. If the result of the decrement is nonzero, the return value is also nonzero but may not equal the result of the decrement.  
  
### Remarks  
 **InterlockedDecrement** prevents more than one thread from simultaneously using this variable.  
  
##  <a name="ccommultithreadmodelnocs__increment"></a>  CComMultiThreadModelNoCS::Increment  
 This static function calls the Win32 function [InterlockedIncrement](http://msdn.microsoft.com/library/windows/desktop/ms683614), which increments the value of the variable pointed to by `p`.  
  
```  
  
static ULONG WINAPI Increment(  
      LPLONG  p  
   ) throw( );  
  
```  
  
### Parameters  
 `p`  
 [in] Pointer to the variable to be incremented.  
  
### Return Value  
 If the result of the increment is 0, then **Increment** returns 0. If the result of the increment is nonzero, the return value is also nonzero but may not equal the result of the increment.  
  
### Remarks  
 **InterlockedIncrement** prevents more than one thread from simultaneously using this variable.  
  
##  <a name="ccommultithreadmodelnocs__threadmodelnocs"></a>  CComMultiThreadModelNoCS::ThreadModelNoCS  
 When using `CComMultiThreadModelNoCS`, the `typedef` name `ThreadModelNoCS` simply references `CComMultiThreadModelNoCS`.  
  
```  
  
typedef CComMultiThreadModelNoCS ThreadModelNoCS;  
  
```  
  
### Remarks  
 [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md) and [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) also contain definitions for `ThreadModelNoCS`. The following table shows the relationship between the threading model class and the class referenced by `ThreadModelNoCS`:  
  
|Class defined in|Class referenced|  
|----------------------|----------------------|  
|`CComMultiThreadModelNoCS`|`CComMultiThreadModelNoCS`|  
|`CComMultiThreadModel`|`CComMultiThreadModelNoCS`|  
|`CComSingleThreadModel`|`CComSingleThreadModel`|  
  
 Note that the definition of `ThreadModelNoCS` in `CComMultiThreadModelNoCS` provides symmetry with `CComMultiThreadModel` and `CComSingleThreadModel`. For example, suppose the sample code in `CComMultiThreadModel::AutoCriticalSection` declared the following `typedef`:  
  
 [!CODE [NVC_ATL_COM#37](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#37)]  
  
 Regardless of the class specified for `ThreadModel` (such as `CComMultiThreadModelNoCS`), `_ThreadModel` resolves accordingly.  
  
### Example  
 See [CComMultiThreadModel::AutoCriticalSection](../vs140/CComMultiThreadModel--AutoCriticalSection.md).  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)