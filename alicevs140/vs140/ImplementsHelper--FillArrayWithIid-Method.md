---
title: "ImplementsHelper::FillArrayWithIid Method"
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
ms.assetid: f60035ee-b7d6-4a08-966d-f88c646944c3
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ImplementsHelper::FillArrayWithIid Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
void FillArrayWithIid(  
   _Inout_ unsigned long *index,   
   _Inout_ IID* iids) throw();  
```  
  
#### Parameters  
 `index`  
 A zero-based index that indicates the starting array element for this operation. When this operation completes, `index` is incremented by 1.  
  
 `iids`  
 An array of type IIDs.  
  
## Remarks  
 Inserts the interface ID specified by the current zeroth template parameter into the specified array element.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [ImplementsHelper Structure](../vs140/ImplementsHelper-Structure.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)