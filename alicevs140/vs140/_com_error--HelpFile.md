---
title: "_com_error::HelpFile"
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
ms.assetid: d2d3a0a1-6b62-4d52-a818-3cfae545a4af
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _com_error::HelpFile
**Microsoft Specific**  
  
 Calls **IErrorInfo::GetHelpFile** function.  
  
## Syntax  
  
```  
  
_bstr_t HelpFile() const;  
  
```  
  
## Return Value  
 Returns the result of **IErrorInfo::GetHelpFile** for the **IErrorInfo** object recorded within the `_com_error` object. The resulting BSTR is encapsulated in a `_bstr_t` object. If no **IErrorInfo** is recorded, it returns an empty `_bstr_t`.  
  
## Remarks  
 Any failure while calling the **IErrorInfo::GetHelpFile** method is ignored.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_com_error Class](../vs140/_com_error-Class.md)