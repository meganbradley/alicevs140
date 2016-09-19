---
title: "_fpieee_flt"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _fpieee_flt
apilocation: 
  - msvcr90.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 2bc4801e-0eed-4e73-b518-215da8cc9740
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _fpieee_flt
Invokes a user-defined trap handler for IEEE floating-point exceptions.  
  
## Syntax  
  
```  
int _fpieee_flt(   
   unsigned long excCode,  
   struct _EXCEPTION_POINTERS *excInfo,  
   int handler(_FPIEEE_RECORD *)   
);  
```  
  
#### Parameters  
 `excCode`  
 Exception code.  
  
 `excInfo`  
 Pointer to the Windows NT exception information structure.  
  
 `handler`  
 Pointer to the user's IEEE trap-handler routine.  
  
## Return Value  
 The return value of `_fpieee_flt` is the value returned by `handler`. As such, the IEEE filter routine might be used in the except clause of a structured exception-handling (SEH) mechanism.  
  
## Remarks  
 The `_fpieee_flt` function invokes a user-defined trap handler for IEEE floating-point exceptions and provides it with all relevant information. This routine serves as an exception filter in the SEH mechanism, which invokes your own IEEE exception handler when necessary.  
  
 The `_FPIEEE_RECORD` structure, defined in Fpieee.h, contains information pertaining to an IEEE floating-point exception. This structure is passed to the user-defined trap handler by `_fpieee_flt`.  
  
|_FPIEEE_RECORD field|Description|  
|----------------------------|-----------------|  
|`unsigned int RoundingMode`, `unsigned int Precision`|These fields contain information about the floating-point environment at the time the exception occurred.|  
|`unsigned int Operation`|Indicates the type of operation that caused the trap. If the type is a comparison (`_FpCodeCompare`), you can supply one of the special `_FPIEEE_COMPARE_RESULT` values (as defined in Fpieee.h) in the `Result.Value` field. The conversion type (`_FpCodeConvert`) indicates that the trap occurred during a floating-point conversion operation. You can look at the `Operand1` and `Result` types to determine the type of conversion being attempted.|  
|`_FPIEEE_VALUE Operand1`, `_FPIEEE_VALUE Operand2`, `_FPIEEE_VALUE Result`|These structures indicate the types and values of the proposed result and operands:<br /><br /> `OperandValid` Flag indicating whether the responding value is valid.<br /><br /> `Format` Data type of the corresponding value. The format type might be returned even if the corresponding value is not valid.<br /><br /> `Value` Result or operand data value.|  
|`_FPIEEE_EXCEPTION_FLAGS Cause`, `_FPIEEE_EXCEPTION_FLAGS Enable`, `_FPIEEE_EXCEPTION_FLAGS Status`|_FPIEEE_EXCEPTION_FLAGS contains one bit field per type of floating point exception.<br /><br /> There is a correspondence between these fields and the arguments used to mask the exceptions supplied to [_controlfp](../vs140/_control87--_controlfp--__control87_2.md).<br /><br /> The exact meaning of each bit depends on context:<br /><br /> `Cause` Each set bit indicates the particular exception that was raised.<br /><br /> `Enable` Each set bit indicates that the particular exception is currently unmasked.<br /><br /> `Status` Each set bit indicates that the particular exception is currently pending. This includes exceptions that have not been raised because they were masked by `_controlfp`.|  
  
 Pending exceptions that are disabled are raised when you enable them. This can result in undefined behavior when using `_fpieee_flt` as an exception filter. Always call [_clearfp](../vs140/_clear87--_clearfp.md) before enabling floating point exceptions.  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_fpieee_flt`|<fpieee.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fpieee.c  
// This program demonstrates the implementation of  
// a user-defined floating-point exception handler using the  
// _fpieee_flt function.  
  
#include <fpieee.h>  
#include <excpt.h>  
#include <float.h>  
#include <stddef.h>  
  
int fpieee_handler( _FPIEEE_RECORD * );  
  
int fpieee_handler( _FPIEEE_RECORD *pieee )  
{  
   // user-defined ieee trap handler routine:  
   // there is one handler for all   
   // IEEE exceptions  
  
   // Assume the user wants all invalid   
   // operations to return 0.  
  
   if ((pieee->Cause.InvalidOperation) &&   
       (pieee->Result.Format == _FpFormatFp32))   
   {  
        pieee->Result.Value.Fp32Value = 0.0F;  
  
        return EXCEPTION_CONTINUE_EXECUTION;  
   }  
   else  
      return EXCEPTION_EXECUTE_HANDLER;  
}  
  
#define _EXC_MASK    \  
    _EM_UNDERFLOW  + \  
    _EM_OVERFLOW   + \  
    _EM_ZERODIVIDE + \  
    _EM_INEXACT  
  
int main( void )  
{  
   // ...  
  
   __try {  
      // unmask invalid operation exception  
      _controlfp_s(NULL, _EXC_MASK, _MCW_EM);   
  
      // code that may generate   
      // fp exceptions goes here  
   }  
   __except ( _fpieee_flt( GetExceptionCode(),  
                GetExceptionInformation(),  
                fpieee_handler ) ){  
  
      // code that gets control   
  
      // if fpieee_handler returns  
      // EXCEPTION_EXECUTE_HANDLER goes here  
  
   }  
  
   // ...  
}  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [_control87, _controlfp, \__control87_2](../vs140/_control87--_controlfp--__control87_2.md)   
 [_controlfp_s](../vs140/_controlfp_s.md)