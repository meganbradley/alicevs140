---
title: "DECLARE_CLASSFACTORY_EX"
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
ms.assetid: 4181ef00-0f30-4e19-b0ee-e7648062e926
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_CLASSFACTORY_EX
Declares `cf` to be the class factory.  
  
## Syntax  
  
```  
  
      DECLARE_CLASSFACTORY_EX(   
   cf    
)  
```  
  
#### Parameters  
 `cf`  
 [in] The name of the class that implements your class factory object.  
  
## Remarks  
 The `cf` parameter must derive from [CComClassFactory](../vs140/CComClassFactory-Class.md) and override the `CreateInstance` method.  
  
 [CComCoClass](../vs140/CComCoClass-Class.md) includes the [DECLARE_CLASSFACTORY](../vs140/DECLARE_CLASSFACTORY.md) macro, which specifies `CComClassFactory` as the default class factory. However, by including the `DECLARE_CLASSFACTORY_EX` macro in your object's class definition, you override this default.  
  
## Example  
 [!CODE [NVC_ATL_COM#8](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#8)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [DECLARE_CLASSFACTORY2](../vs140/DECLARE_CLASSFACTORY2.md)   
 [DECLARE_CLASSFACTORY_AUTO_THREAD](../vs140/DECLARE_CLASSFACTORY_AUTO_THREAD.md)   
 [DECLARE_CLASSFACTORY_SINGLETON](../vs140/DECLARE_CLASSFACTORY_SINGLETON.md)