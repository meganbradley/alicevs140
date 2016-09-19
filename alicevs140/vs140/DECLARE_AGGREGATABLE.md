---
title: "DECLARE_AGGREGATABLE"
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
ms.assetid: e7e568d7-04e0-4226-b5dc-224deed229ab
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_AGGREGATABLE
Specifies that your object can be aggregated.  
  
## Syntax  
  
```  
  
      DECLARE_AGGREGATABLE(   
   x    
)  
```  
  
#### Parameters  
 *x*  
 [in] The name of the class you are defining as aggregatable.  
  
## Remarks  
 [CComCoClass](../vs140/CComCoClass-Class.md) contains this macro to specify the default aggregation model. To override this default, specify either the [DECLARE_NOT_AGGREGATABLE](../vs140/DECLARE_NOT_AGGREGATABLE.md) or [DECLARE_ONLY_AGGREGATABLE](../vs140/DECLARE_ONLY_AGGREGATABLE.md) macro in your class definition.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#121](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#121)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)