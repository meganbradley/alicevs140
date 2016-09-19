---
title: "Implementing CComObject, CComAggObject, and CComPolyObject"
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
ms.topic: article
ms.assetid: 5aabe938-104d-492e-9c41-9f7fb1c62098
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implementing CComObject, CComAggObject, and CComPolyObject
The template classes [CComObject](../vs140/CComObject-Class.md), [CComAggObject](../vs140/CComAggObject-Class.md), and [CComPolyObject](../vs140/CComPolyObject-Class.md) are always the most derived classes in the inheritance chain. It is their responsibility to handle all of the methods in **IUnknown**: `QueryInterface`, `AddRef`, and **Release**. In addition, `CComAggObject` and `CComPolyObject` (when used for aggregated objects) provide the special reference counting and `QueryInterface` semantics required for the inner unknown.  
  
 Whether `CComObject`, `CComAggObject`, or `CComPolyObject` is used depends on whether you declare one (or none) of the following macros:  
  
|Macro|Effect|  
|-----------|------------|  
|`DECLARE_NOT_AGGREGATABLE`|Always uses `CComObject`.|  
|`DECLARE_AGGREGATABLE`|Uses `CComAggObject` if the object is aggregated and `CComObject` if it is not. `CComCoClass` contains this macro so if none of the **DECLARE_\*_AGGREGATABLE** macros are declared in your class, this will be the default.|  
|`DECLARE_ONLY_AGGREGATABLE`|Always uses `CComAggObject`. Returns an error if the object is not aggregated.|  
|`DECLARE_POLY_AGGREGATABLE`|ATL creates an instance of **CComPolyObject<CYourClass\>** when **IClassFactory::CreateInstance** is called. During creation, the value of the outer unknown is checked. If it is **NULL**, **IUnknown** is implemented for a nonaggregated object. If the outer unknown is not **NULL**, **IUnknown** is implemented for an aggregated object.|  
  
 The advantage of using `CComAggObject` and `CComObject` is that the implementation of **IUnknown** is optimized for the kind of object being created. For instance, a nonaggregated object only needs a reference count, while an aggregated object needs both a reference count for the inner unknown and a pointer to the outer unknown.  
  
 The advantage of using `CComPolyObject` is that you avoid having both `CComAggObject` and `CComObject` in your module to handle the aggregated and nonaggregated cases. A single `CComPolyObject` object handles both cases. This means only one copy of the vtable and one copy of the functions exist in your module. If your vtable is large, this can substantially decrease your module size. However, if your vtable is small, using `CComPolyObject` can result in a slightly larger module size because it is not optimized for an aggregated or nonaggregated object, as are `CComAggObject` and `CComObject`.  
  
## See Also  
 [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md)   
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)