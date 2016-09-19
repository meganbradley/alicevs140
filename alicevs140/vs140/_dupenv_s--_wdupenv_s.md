---
title: "_dupenv_s, _wdupenv_s"
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
  - _dupenv_s
  - _wdupenv_s
apilocation: 
  - msvcr90.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: b729ecc2-a31d-4ccf-92a7-5accedb8f8c8
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _dupenv_s, _wdupenv_s
Gets a value from the current environment.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
errno_t _dupenv_s(  
   char **buffer,  
   size_t *numberOfElements,  
   const char *varname  
);  
errno_t _wdupenv_s(  
   wchar_t **buffer,  
   size_t *numberOfElements,  
   const wchar_t *varname  
);  
```  
  
#### Parameters  
 `buffer`  
 Buffer to store the variable's value.  
  
 `numberOfElements`  
 Size of `buffer`.  
  
 `varname`  
 Environment variable name.  
  
## Return Value  
 Zero on success, an error code on failure.  
  
 These functions validate their parameters; if `buffer` or `varname` is `NULL`, the invalid parameter handler is invoked as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the functions set `errno` to `EINVAL` and return `EINVAL`.  
  
 If these functions cannot allocate enough memory, they set `buffer` to `NULL` and `numberOfElements` to 0, and return `ENOMEM`.  
  
## Remarks  
 The `_dupenv_s` function searches the list of environment variables for `varname`. If the variable is found, `_dupenv_s` allocates a buffer and copies the variable's value into the buffer. The buffer's address and length are returned in `buffer` and `numberOfElements`. By allocating the buffer itself, `_dupenv_s` provides a more convenient alternative to [getenv_s, _wgetenv_s](../vs140/getenv_s--_wgetenv_s.md).  
  
> [!NOTE]
>  It is the calling program's responsibility to free the memory by calling [free](../vs140/free.md).  
  
 If the variable is not found, then `buffer` is set to `NULL`, `numberOfElements` is set to 0, and the return value is 0 because this situation is not considered to be an error condition.  
  
 If you are not interested in the size of the buffer you can pass `NULL` for `numberOfElements`.  
  
 `_dupenv_s` is not case sensitive in the Windows operating system. `_dupenv_s` uses the copy of the environment pointed to by the global variable `_environ` to access the environment. See the Remarks in [getenv_s, _wgetenv_s](../vs140/getenv_s--_wgetenv_s.md) for a discussion of `_environ`.  
  
 The value in `buffer` is a copy of the environment variable's value; modifying it has no effect on the environment. Use the [putenv_s](../vs140/_putenv_s--_wputenv_s.md) function to modify the value of an environment variable.  
  
 `_wdupenv_s` is a wide-character version of `_dupenv_s`; the arguments of `_wdupenv_s` are wide-character strings. The `_wenviron` global variable is a wide-character version of `_environ`. See the Remarks in [getenv_s, _wgetenv_s](../vs140/getenv_s--_wgetenv_s.md) for more on `_wenviron`.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tdupenv_s`|`_dupenv_s`|`_dupenv_s`|`_wdupenv_s`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_dupenv_s`|<stdlib.h>|  
|`_wdupenv_s`|<stdlib.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_dupenv_s.c  
#include  <stdlib.h>  
  
int main( void )  
{  
   char *pValue;  
   size_t len;  
   errno_t err = _dupenv_s( &pValue, &len, "pathext" );  
   if ( err ) return -1;  
   printf( "pathext = %s\n", pValue );  
   free( pValue );  
   err = _dupenv_s( &pValue, &len, "nonexistentvariable" );  
   if ( err ) return -1;  
   printf( "nonexistentvariable = %s\n", pValue );  
   free( pValue ); // It's OK to call free with NULL  
}  
```  
  
## Sample Output  
  
```  
pathext = .COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.pl  
nonexistentvariable = (null)  
```  
  
## .NET Framework Equivalent  
 [System::Environment::GetEnvironmentVariable](https://msdn.microsoft.com/en-us/library/system.environment.getenvironmentvariable.aspx)  
  
## See Also  
 [Process and Environment Control](../vs140/Process-and-Environment-Control.md)   
 [Environmental Constants](../vs140/Environmental-Constants.md)   
 [_dupenv_s_dbg, _wdupenv_s_dbg](../vs140/_dupenv_s_dbg--_wdupenv_s_dbg.md)   
 [getenv_s, _wgetenv_s](../vs140/getenv_s--_wgetenv_s.md)   
 [putenv_s, _wputenv_s](../vs140/_putenv_s--_wputenv_s.md)