---
title: "Changing the Default Class Factory and Aggregation Model"
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
ms.assetid: 6e040e95-0f38-4839-8a8b-c9800dd47e8c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Changing the Default Class Factory and Aggregation Model
ATL uses [CComCoClass](../vs140/CComCoClass-Class.md) to define the default class factory and aggregation model for your object. `CComCoClass` specifies the following two macros:  
  
-   [DECLARE_CLASSFACTORY](../vs140/DECLARE_CLASSFACTORY.md) Declares the class factory to be [CComClassFactory](../vs140/CComClassFactory-Class.md).  
  
-   [DECLARE_AGGREGATABLE](../vs140/DECLARE_AGGREGATABLE.md) Declares that your object can be aggregated.  
  
 You can override either of these defaults by specifying another macro in your class definition. For example, to use [CComClassFactory2](../vs140/CComClassFactory2-Class.md) instead of `CComClassFactory`, specify the [DECLARE_CLASSFACTORY2](../vs140/DECLARE_CLASSFACTORY2.md) macro:  
  
 [!CODE [NVC_ATL_COM#2](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#2)]  
  
 Two other macros that define a class factory are [DECLARE_CLASSFACTORY_AUTO_THREAD](../vs140/DECLARE_CLASSFACTORY_AUTO_THREAD.md) and [DECLARE_CLASSFACTORY_SINGLETON](../vs140/DECLARE_CLASSFACTORY_SINGLETON.md).  
  
 ATL also uses the `typedef` mechanism to implement default behavior. For example, the `DECLARE_AGGREGATABLE` macro uses `typedef` to define a type called **_CreatorClass**, which is then referenced throughout ATL. Note that in a derived class, a `typedef` using the same name as the base class's `typedef` results in ATL using your definition and overriding the default behavior.  
  
## See Also  
 [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md)   
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)