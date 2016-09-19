---
title: "CComSingleThreadModel::ThreadModelNoCS"
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
ms.assetid: ff1209bf-df35-40d0-a213-7a68969d3bdf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSingleThreadModel::ThreadModelNoCS
When using `CComSingleThreadModel`, the `typedef` name `ThreadModelNoCS` simply references `CComSingleThreadModel`.  
  
## Syntax  
  
```  
  
typedef CComSingleThreadModel ThreadModelNoCS;  
  
```  
  
## Remarks  
 [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md) and [CComMultiThreadModelNoCS](../vs140/CComMultiThreadModelNoCS-Class.md) contain definitions for `ThreadModelNoCS`. The following table shows the relationship between the threading model class and the class referenced by `ThreadModelNoCS`:  
  
|Class defined in|Class referenced|  
|----------------------|----------------------|  
|`CComSingleThreadModel`|`CComSingleThreadModel`|  
|`CComMultiThreadModel`|`CComMultiThreadModelNoCS`|  
|`CComMultiThreadModelNoCS`|`CComMultiThreadModelNoCS`|  
  
## Example  
 See [CComMultiThreadModel::AutoCriticalSection](../vs140/CComMultiThreadModel--AutoCriticalSection.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComSingleThreadModel Class](../vs140/CComSingleThreadModel-Class.md)   
 [CComObjectThreadModel](../vs140/CComObjectThreadModel.md)   
 [CComGlobalsThreadModel](../vs140/CComGlobalsThreadModel.md)