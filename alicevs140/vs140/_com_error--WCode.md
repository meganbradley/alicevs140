---
title: "_com_error::WCode"
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
ms.assetid: f3b21852-f8ea-4e43-bff1-11c2d35454c4
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _com_error::WCode
**Microsoft Specific**  
  
 Retrieves the 16-bit error code mapped into the encapsulated `HRESULT`.  
  
## Syntax  
  
```  
  
WORD WCode ( ) const throw( );  
  
```  
  
## Return Value  
 If the `HRESULT` is within the range 0x80040200 to 0x8004FFFF, the **WCode** method returns the `HRESULT` minus 0x80040200; otherwise, it returns zero.  
  
## Remarks  
 The **WCode** method is used to undo a mapping that happens in the COM support code. The wrapper for a **dispinterface** property or method calls a support routine that packages the arguments and calls **IDispatch::Invoke**. Upon return, if a failure `HRESULT` of `DISP_E_EXCEPTION` is returned, the error information is retrieved from the **EXCEPINFO** structure passed to **IDispatch::Invoke**. The error code can either be a 16-bit value stored in the `wCode` member of the **EXCEPINFO** structure or a full 32-bit value in the **scode** member of the **EXCEPINFO** structure. If a 16-bit `wCode` is returned, it must first be mapped to a 32-bit failure `HRESULT`.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_com_error::HRESULTToWCode](../vs140/_com_error--HRESULTToWCode.md)   
 [_com_error::WCodeToHRESULT](../vs140/_com_error--WCodeToHRESULT.md)   
 [_com_error Class](../vs140/_com_error-Class.md)