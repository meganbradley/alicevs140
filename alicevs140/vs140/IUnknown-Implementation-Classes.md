---
title: "IUnknown Implementation Classes"
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
ms.assetid: 47b69bb5-69d8-4a9c-84a8-329bdde2bb3f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IUnknown Implementation Classes
The following classes implement **IUnknown** and related methods:  
  
-   [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md) Manages reference counting for both aggregated and nonaggregated objects. Allows you to specify a threading model.  
  
-   [CComObjectRoot](../vs140/CComObjectRoot-Class.md) Manages reference counting for both aggregated and nonaggregated objects. Uses the default threading model of the server.  
  
-   [CComAggObject](../vs140/CComAggObject-Class.md) Implements **IUnknown** for an aggregated object.  
  
-   [CComObject](../vs140/CComObject-Class.md) Implements **IUnknown** for a nonaggregated object.  
  
-   [CComPolyObject](../vs140/CComPolyObject-Class.md) Implements **IUnknown** for aggregated and nonaggregated objects. Using `CComPolyObject` avoids having both `CComAggObject` and `CComObject` in your module. A single `CComPolyObject` object handles both aggregated and nonaggregated cases.  
  
-   [CComObjectNoLock](../vs140/CComObjectNoLock-Class.md) Implements **IUnknown** for a nonaggregated object, without modifying the module lock count.  
  
-   [CComTearOffObject](../vs140/CComTearOffObject-Class.md) Implements **IUnknown** for a tear-off interface.  
  
-   [CComCachedTearOffObject](../vs140/CComCachedTearOffObject-Class.md) Implements **IUnknown** for a "cached" tear-off interface.  
  
-   [CComContainedObject](../vs140/CComContainedObject-Class.md) Implements **IUnknown** for the inner object of an aggregation or a tear-off interface.  
  
-   [CComObjectGlobal](../vs140/CComObjectGlobal-Class.md) Manages a reference count on the module to ensure your object won't be deleted.  
  
-   [CComObjectStack](../vs140/CComObjectStack-Class.md) Creates a temporary COM object, using a skeletal implementation of **IUnknown**.  
  
## Related Articles  
 [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md)  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)   
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [COM Map Global Functions](../vs140/COM-Map-Global-Functions.md)