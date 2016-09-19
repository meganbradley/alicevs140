---
title: "_cgets_s, _cgetws_s"
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
  - _cgetws_s
  - _cgets_s
apilocation: 
  - msvcr100.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 38b74897-afe6-4dd9-a43f-36a3c0d72c5c
caps.latest.revision: 33
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _cgets_s, _cgetws_s
Gets a character string from the console. These versions of [_cgets and _cgetws](../vs140/_cgets--_cgetws.md) have security enhancements, as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
errno_t _cgets_s(   
   char *buffer,  
   size_t numberOfElements,  
   size_t *pSizeRead  
);  
errno_t _cgetws_s(  
   wchar_t *buffer  
   size_t numberOfElements,  
   size_t *pSizeRead  
);  
template <size_t size>  
errno_t _cgets_s(   
   char (&buffer)[size],  
   size_t *pSizeRead  
); // C++ only  
template <size_t size>  
errno_t _cgetws_s(  
   wchar_t (&buffer)[size],  
   size_t *pSizeRead  
); // C++ only  
```  
  
#### Parameters  
 [out] `buffer`  
 Storage location for data.  
  
 [in] `numberOfElements`  
 The size of the buffer in single-byte or wide characters, which is also the maximum number of characters to be read.  
  
 [in] `pSizeRead`  
 The number of characters actually read.  
  
## Return Value  
 The return value is zero if successful; otherwise, an error code if a failure occurs.  
  
### Error Conditions  
  
|`buffer`|`numberOfElements`|`pSizeRead`|Return|Contents of `buffer`|  
|--------------|------------------------|-----------------|------------|--------------------------|  
|`NULL`|any|any|`EINVAL`|n/a|  
|not `NULL`|zero|any|`EINVAL`|not modified|  
|not `NULL`|any|`NULL`|`EINVAL`|zero-length string|  
  
## Remarks  
 `_cgets_s` and `_cgetws_s` read a string from the console and copy the string (with a null terminator) into `buffer`. `_cgetws_s` is the wide character version of the function; other than the character size, the behavior of these two functions is identical. The maximum size of the string to be read is passed in as the `numberOfElements` parameter. This size should include an extra character for the terminating null. The actual number of characters read is placed in `pSizeRead`.  
  
 If an error occurs during the operation or in the validating of the parameters, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md) . If execution is allowed to continue, `errno` is set to `EINVAL` and `EINVAL` is returned.  
  
 In C++, the use of these functions is simplified by template overloads; the overloads can infer buffer length automatically, thereby eliminating the need to specify a size argument, and they can automatically replace older, less-secure functions with their newer, more secure counterparts. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_cgetts_s`|`_cgets_s`|`_cgets_s`|`_cgetws_s`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_cgets_s`|<conio.h>|  
|`_cgetws_s`|<conio.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Console and Port I/O](../vs140/Console-and-Port-I-O.md)   
 [_getch, _getwch](../vs140/_getch--_getwch.md)