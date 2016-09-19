---
title: "DECLARE_ONLY_AGGREGATABLE"
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
ms.assetid: a54220df-4330-4e4d-b7fb-8b63dd62d337
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_ONLY_AGGREGATABLE
Specifies that your object must be aggregated.  
  
## Syntax  
  
```  
  
      DECLARE_ONLY_AGGREGATABLE(   
   x    
)  
```  
  
#### Parameters  
 *x*  
 [in] The name of the class object you are defining as only aggregatable.  
  
## Remarks  
 `DECLARE_ONLY_AGGREGATABLE` causes an error (**E_FAIL**) if an attempt is made to **CoCreate** your object as nonaggregated object.  
  
 By default, [CComCoClass](../vs140/CComCoClass-Class.md) contains the [DECLARE_AGGREGATABLE](../vs140/DECLARE_AGGREGATABLE.md) macro, which specifies that your object can be aggregated. To override this default behavior, include `DECLARE_ONLY_AGGREGATABLE` in your class definition.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#125](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#125)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [DECLARE_NOT_AGGREGATABLE](../vs140/DECLARE_NOT_AGGREGATABLE.md)