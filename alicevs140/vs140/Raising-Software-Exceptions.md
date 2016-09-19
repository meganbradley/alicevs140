---
title: "Raising Software Exceptions"
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
ms.assetid: be1376c3-c46a-4f52-ad1d-c2362840746a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Raising Software Exceptions
Some of the most common sources of program errors are not flagged as exceptions by the system. For example, if you attempt to allocate a memory block but there is insufficient memory, the run-time or API function does not raise an exception but returns an error code.  
  
 However, you can treat any condition as an exception by detecting that condition in your code and then reporting it by calling the [RaiseException](http://msdn.microsoft.com/library/windows/desktop/ms680552) function. By flagging errors this way, you can bring the advantages of structured exception handling to any kind of run-time error.  
  
 To use structured exception handling with errors:  
  
-   Define your own exception code for the event.  
  
-   Call **RaiseException** when you detect a problem.  
  
-   Use exception-handling filters to test for the exception code you defined.  
  
 The WINERROR.H file shows the format for exception codes. To make sure that you do not define a code that conflicts with an existing exception code, set the third most significant bit to 1. The four most-significant bits should be set as shown in the following table.  
  
|Bits|Recommended binary setting|Description|  
|----------|--------------------------------|-----------------|  
|31-30|11|These two bits describe the basic status of the code:  11 = error, 00 = success, 01 = informational, 10 = warning.|  
|29|1|Client bit. Set to 1 for user-defined codes.|  
|28|0|Reserved bit. (Leave set to 0.)|  
  
 You can set the first two bits to a setting other than 11 binary if you want, although the "error" setting is appropriate for most exceptions. The important thing to remember is to set bits 29 and 28 as shown in the previous table.  
  
 The resulting error code should therefore have the highest four bits set to hexadecimal E. For example, the following definitions define exception codes that do not conflict with any Windows exception codes. (You may, however, need to check which codes are used by third-party DLLs.)  
  
```  
#define STATUS_INSUFFICIENT_MEM       0xE0000001  
#define STATUS_FILE_BAD_FORMAT        0xE0000002  
```  
  
 After you have defined an exception code, you can use it to raise an exception. For example, the following code raises the STATUS_INSUFFICIENT_MEM exception in response to a memory allocation problem:  
  
```  
lpstr = _malloc( nBufferSize );  
if (lpstr == NULL)  
    RaiseException( STATUS_INSUFFICIENT_MEM, 0, 0, 0);  
```  
  
 If you want to simply raise an exception, you can set the last three parameters to 0. The three last parameters are useful for passing additional information and setting a flag that prevents handlers from continuing execution. See the [RaiseException](http://msdn.microsoft.com/library/windows/desktop/ms680552) function in the [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)] for more information.  
  
 In your exception-handling filters, you can then test for the codes you've defined. For example:  
  
```  
__try {  
    ...  
}  
__except (GetExceptionCode() == STATUS_INSUFFICIENT_MEM ||  
        GetExceptionCode() == STATUS_FILE_BAD_FORMAT )  
```  
  
## See Also  
 [Writing an Exception Handler](../vs140/Writing-an-Exception-Handler.md)   
 [Structured Exception Handling (C/C++)](../vs140/Structured-Exception-Handling--C-C---.md)