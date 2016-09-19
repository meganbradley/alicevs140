---
title: "_com_error::Description"
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
ms.topic: language-reference
ms.assetid: 88191e24-4ee8-44a6-8c4c-3758e22e0548
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _com_error::Description
**Microsoft Specific**  
  
 Calls **IErrorInfo::GetDescription** function.  
  
## Syntax  
  
```  
  
_bstr_t Description( ) const;  
  
```  
  
## Return Value  
 Returns the result of **IErrorInfo::GetDescription** for the **IErrorInfo** object recorded within the `_com_error` object. The resulting `BSTR` is encapsulated in a `_bstr_t` object. If no **IErrorInfo** is recorded, it returns an empty `_bstr_t`.  
  
## Remarks  
 Calls the **IErrorInfo::GetDescription** function and retrieves **IErrorInfo** recorded within the `_com_error` object. Any failure while calling the **IErrorInfo::GetDescription** method is ignored.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_com_error Class](../vs140/_com_error-Class.md)