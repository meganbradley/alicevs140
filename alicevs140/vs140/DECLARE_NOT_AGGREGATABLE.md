---
title: "DECLARE_NOT_AGGREGATABLE"
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
ms.assetid: 2a116c7c-bab8-4f2a-a9ad-03d7aba0f762
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_NOT_AGGREGATABLE
Specifies that your object cannot be aggregated.  
  
## Syntax  
  
```  
  
      DECLARE_NOT_AGGREGATABLE(   
   x    
)  
```  
  
#### Parameters  
 *x*  
 [in] The name of the class object you are defining as not aggregatable.  
  
## Remarks  
 `DECLARE_NOT_AGGREGATABLE` causes `CreateInstance` to return an error (**CLASS_E_NOAGGREGATION**) if an attempt is made to aggregate onto your object.  
  
 By default, [CComCoClass](../vs140/CComCoClass-Class.md) contains the [DECLARE_AGGREGATABLE](../vs140/DECLARE_AGGREGATABLE.md) macro, which specifies that your object can be aggregated. To override this default behavior, include `DECLARE_NOT_AGGREGATABLE` in your class definition.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#121](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#121)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [DECLARE_ONLY_AGGREGATABLE](../vs140/DECLARE_ONLY_AGGREGATABLE.md)