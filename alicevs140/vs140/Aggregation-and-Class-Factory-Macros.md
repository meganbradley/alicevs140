---
title: "Aggregation and Class Factory Macros"
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
ms.assetid: d99d379a-0eec-481f-8daa-252dac18f163
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Aggregation and Class Factory Macros
These macros provide ways of controlling aggregation and of declaring class factories.  
  
|||  
|-|-|  
|[DECLARE_AGGREGATABLE](../vs140/DECLARE_AGGREGATABLE.md)|Declares that your object can be aggregated (the default).|  
|[DECLARE_CLASSFACTORY](../vs140/DECLARE_CLASSFACTORY.md)|Declares the class factory to be [CComClassFactory](../vs140/CComClassFactory-Class.md), the ATL default class factory.|  
|[DECLARE_CLASSFACTORY_EX](../vs140/DECLARE_CLASSFACTORY_EX.md)|Declares your class factory object to be the class factory.|  
|[DECLARE_CLASSFACTORY2](../vs140/DECLARE_CLASSFACTORY2.md)|Declares [CComClassFactory2](../vs140/CComClassFactory2-Class.md) to be the class factory.|  
|[DECLARE_CLASSFACTORY_AUTO_THREAD](../vs140/DECLARE_CLASSFACTORY_AUTO_THREAD.md)|Declares [CComClassFactoryAutoThread](../vs140/CComClassFactoryAutoThread-Class.md) to be the class factory.|  
|[DECLARE_CLASSFACTORY_SINGLETON](../vs140/DECLARE_CLASSFACTORY_SINGLETON.md)|Declares [CComClassFactorySingleton](../vs140/CComClassFactorySingleton-Class.md) to be the class factory.|  
|[DECLARE_GET_CONTROLLING_UNKNOWN](../vs140/DECLARE_GET_CONTROLLING_UNKNOWN.md)|Declares a virtual `GetControllingUnknown` function.|  
|[DECLARE_NOT_AGGREGATABLE](../vs140/DECLARE_NOT_AGGREGATABLE.md)|Declares that your object cannot be aggregated.|  
|[DECLARE_ONLY_AGGREGATABLE](../vs140/DECLARE_ONLY_AGGREGATABLE.md)|Declares that your object must be aggregated.|  
|[DECLARE_POLY_AGGREGATABLE](../vs140/DECLARE_POLY_AGGREGATABLE.md)|Checks the value of the outer unknown and declares your object aggregatable or not aggregatable, as appropriate.|  
|[DECLARE_PROTECT_FINAL_CONSTRUCT](../vs140/DECLARE_PROTECT_FINAL_CONSTRUCT.md)|Protects the outer object from deletion during construction of an inner object.|  
|[DECLARE_VIEW_STATUS](../vs140/DECLARE_VIEW_STATUS.md)|Specifies the **VIEWSTATUS** flags to the container.|  
  
## See Also  
 [Macros](../vs140/ATL-Macros.md)