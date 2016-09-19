---
title: "DECLARE_CLASSFACTORY_AUTO_THREAD"
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
ms.assetid: 19d7105e-03e8-4412-9f5e-5384c8a5e18f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_CLASSFACTORY_AUTO_THREAD
Declares [CComClassFactoryAutoThread](../vs140/CComClassFactoryAutoThread-Class.md) to be the class factory.  
  
## Syntax  
  
```  
  
DECLARE_CLASSFACTORY_AUTO_THREAD( )  
  
```  
  
## Remarks  
 [CComCoClass](../vs140/CComCoClass-Class.md) includes the [DECLARE_CLASSFACTORY](../vs140/DECLARE_CLASSFACTORY.md) macro, which specifies [CComClassFactory](../vs140/CComClassFactory-Class.md) as the default class factory. However, by including the `DECLARE_CLASSFACTORY_AUTO_THREAD` macro in your object's class definition, you override this default.  
  
 When you create objects in multiple apartments (in an out-of-proc server), add `DECLARE_CLASSFACTORY_AUTO_THREAD` to your class.  
  
## Example  
 [!CODE [NVC_ATL_COM#9](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#9)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [DECLARE_CLASSFACTORY_EX](../vs140/DECLARE_CLASSFACTORY_EX.md)   
 [DECLARE_CLASSFACTORY2](../vs140/DECLARE_CLASSFACTORY2.md)   
 [DECLARE_CLASSFACTORY_SINGLETON](../vs140/DECLARE_CLASSFACTORY_SINGLETON.md)