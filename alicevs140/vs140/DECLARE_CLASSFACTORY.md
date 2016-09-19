---
title: "DECLARE_CLASSFACTORY"
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
ms.assetid: 51a6b925-07c0-4d3a-9174-0b8c808975e4
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_CLASSFACTORY
Declares [CComClassFactory](../vs140/CComClassFactory-Class.md) to be the class factory.  
  
## Syntax  
  
```  
  
DECLARE_CLASSFACTORY( )  
  
```  
  
## Remarks  
 [CComCoClass](../vs140/CComCoClass-Class.md) uses this macro to declare the default class factory for your object.  
  
## Example  
 [!CODE [NVC_ATL_COM#55](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#55)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [DECLARE_CLASSFACTORY_EX](../vs140/DECLARE_CLASSFACTORY_EX.md)   
 [DECLARE_CLASSFACTORY2](../vs140/DECLARE_CLASSFACTORY2.md)   
 [DECLARE_CLASSFACTORY_AUTO_THREAD](../vs140/DECLARE_CLASSFACTORY_AUTO_THREAD.md)   
 [DECLARE_CLASSFACTORY_SINGLETON](../vs140/DECLARE_CLASSFACTORY_SINGLETON.md)