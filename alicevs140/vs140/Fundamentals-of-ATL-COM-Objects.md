---
title: "Fundamentals of ATL COM Objects"
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
ms.assetid: 0f9c9d98-cc28-45da-89ac-dc94cee422fe
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fundamentals of ATL COM Objects
The following illustration depicts the relationship among the classes and interfaces that are used to define an ATL COM object.  
  
 ![ATL structure](../vs140/media/vc307Y1.gif "vc307Y1")  
  
> [!NOTE]
>  This diagram shows that `CComObject` is derived from `CYourClass` whereas `CComAggObject` and `CComPolyObject` include `CYourClass` as a member variable.  
  
 There are three ways to define an ATL COM object. The standard option is to use the `CComObject` class which is derived from `CYourClass`. The second option is to create an aggregated object by using the `CComAggObject` class. The third option is to use the `CComPolyObject` class. `CComPolyObject` acts as a hybrid: it can function as a `CComObject` class or as a `CComAggObject` class, depending on how it is first created. For more information about how to use the `CComPolyObject` class, see [CComPolyObject Class](../vs140/CComPolyObject-Class.md).  
  
 When you use standard ATL COM, you use two objects: an outer object and an inner object. External clients access the functionality of the inner object through the wrapper functions that are defined in the outer object. The outer object is of type `CComObject`.  
  
 When you use an aggregated object, the outer object does not provide wrappers for the functionality of the inner object. Instead, the outer object provides a pointer that is directly accessed by external clients. In this scenario, the outer object is of type `CComAggObject`. The inner object is a member variable of the outer object, and it is of type `CYourClass`.  
  
 Because the client does not have to go through the outer object to interact with the inner object, aggregated objects are usually more efficient. Also, the outer object does not have to know the functionality of the aggregated object, given that the interface of the aggregated object is directly available to the client. However, not all objects can be aggregated. For an object to be aggregated, it needs to be designed with aggregation in mind.  
  
 ATL implements [IUnknown](http://msdn.microsoft.com/library/windows/desktop/ms680509) in two phases:  
  
-   [CComObject](../vs140/CComObject-Class.md), [CComAggObject](../vs140/CComAggObject-Class.md), or [CComPolyObject](../vs140/CComPolyObject-Class.md) implements the **IUnknown** methods.  
  
-   [CComObjectRoot](../vs140/CComObjectRoot-Class.md) or [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md) manages the reference count and outer pointers of **IUnknown**.  
  
 Other aspects of your ATL COM object are handled by other classes:  
  
-   [CComCoClass](../vs140/CComCoClass-Class.md) defines the object's default class factory and aggregation model.  
  
-   [IDispatchImpl](../vs140/IDispatchImpl-Class.md) provides a default implementation of the `IDispatch Interface` portion of any dual interfaces on the object.  
  
-   [ISupportErrorInfoImpl](../vs140/ISupportErrorInfoImpl-Class.md) implements the **ISupportErrorInfo** interface that ensures error information can be propagated up the call chain correctly.  
  
## In This Section  
 [Implementing CComObjectRootEx](../vs140/Implementing-CComObjectRootEx.md)  
 Show example COM map entries for implementing `CComObjectRootEx`.  
  
 [Implementing CComObject, CComAggObject, and CComPolyObject](../vs140/Implementing-CComObject--CComAggObject--and-CComPolyObject.md)  
 Discusses how the **DECLARE_\*_AGGREGATABLE** macros affect the use of `CComObject`, `CComAggObject`, and `CComPolyObject`.  
  
 [Supporting IDispatch and IErrorInfo](../vs140/Supporting-IDispatch-and-IErrorInfo.md)  
 Lists the ATL implementation classes to use for supporting the `IDispatch` and **IErrorInfo** interfaces.  
  
 [Supporting IDispEventImpl](../vs140/Supporting-IDispEventImpl.md)  
 Discusses the steps to implement a connection point for your class.  
  
 [Changing the Default Class Factory and Aggregation Model](../vs140/Changing-the-Default-Class-Factory-and-Aggregation-Model.md)  
 Show what macros to use to change the default class factory and aggregation model.  
  
 [Creating an Aggregated Object](../vs140/Creating-an-Aggregated-Object.md)  
 Lists the steps for creating an aggregated object.  
  
## Related Sections  
 [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md)  
 Provides information about creating an ATL COM object.  
  
 [ATL](../vs140/Active-Template-Library--ATL--Concepts.md)  
 Provides links to conceptual topics on how to program using the Active Template Library.  
  
## See Also  
 [ATL](../vs140/Active-Template-Library--ATL--Concepts.md)