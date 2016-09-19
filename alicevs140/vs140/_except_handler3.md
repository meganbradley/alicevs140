---
title: "_except_handler3"
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
ms.topic: article
apiname: 
  - _except_handler3
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: b0c64898-0ae5-48b7-9724-80135a0813e2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _except_handler3
Internal CRT function. Used by a framework to find the appropriate exception handler to process the current exception.  
  
## Syntax  
  
```  
int _except_handler3(  
   PEXCEPTION_RECORD exception_record,  
   PEXCEPTION_REGISTRATION registration,  
   PCONTEXT context,  
   PEXCEPTION_REGISTRATION dispatcher  
);  
```  
  
#### Parameters  
 [in] `exception_record`  
 Information about the specific exception.  
  
 [in] `registration`  
 The record that indicates which scope table should be used to find the exception handler.  
  
 [in] `context`  
 Reserved.  
  
 [in] `dispatcher`  
 Reserved.  
  
## Return Value  
 If an exception should be dismissed, returns `DISPOSITION_DISMISS`. If the exception should be passed up a level to the encapsulating exception handlers, returns `DISPOSITION_CONTINUE_SEARCH`.  
  
## Remarks  
 If this method finds an appropriate exception handler, it passes the exception to the handler. In this situation, this method does not return to the code that called it and the return value is irrelevant.  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)