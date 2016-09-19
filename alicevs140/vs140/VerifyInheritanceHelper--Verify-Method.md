---
title: "VerifyInheritanceHelper::Verify Method"
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
ms.assetid: 3360082b-81ad-4191-9ec3-b4372f7207d7
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VerifyInheritanceHelper::Verify Method
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
static void Verify();  
```  
  
## Remarks  
 Tests the two interfaces specified by the current template parameters and determines whether one interface is derived from the other.  
  
 An error is emitted if one interface is not derived from the other.  
  
## Requirements  
 **Header:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [VerifyInheritanceHelper Structure](../vs140/VerifyInheritanceHelper-Structure.md)   
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)