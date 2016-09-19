---
title: "InvokeHelper::InvokeHelper Constructor"
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
ms.assetid: 0223c574-abc3-4fc0-99e6-38626ba79243
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# InvokeHelper::InvokeHelper Constructor
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
explicit InvokeHelper(  
   TCallback callback  
);  
```  
  
#### Parameters  
 `callback`  
 An event handler.  
  
## Remarks  
 Initializes a new instance of the InvokeHelper class.  
  
 The `TCallback` template parameter specifies the type of the event handler.  
  
## Requirements  
 **Header:** event.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [InvokeHelper Structure](../vs140/InvokeHelper-Structure.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)