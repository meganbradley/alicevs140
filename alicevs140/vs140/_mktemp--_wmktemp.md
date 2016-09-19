---
title: "_mktemp, _wmktemp"
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
  - _wmktemp
  - _mktemp
apilocation: 
  - msvcr80.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 055eb539-a8c2-4a7d-be54-f5b6d1eb5c85
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mktemp, _wmktemp
Creates a unique file name. More secure versions of these functions are available; see [_mktemp_s, _wmktemp_s](../vs140/_mktemp_s--_wmktemp_s.md).  
  
## Syntax  
  
```  
char *_mktemp(  
   char *template   
);  
wchar_t *_wmktemp(  
   wchar_t *template   
);  
template <size_t size>  
char *_mktemp(  
   char (&template)[size]  
); // C++ only  
template <size_t size>  
wchar_t *_wmktemp(  
   wchar_t (&template)[size]  
); // C++ only  
```  
  
#### Parameters  
 `template`  
 File name pattern.  
  
## Return Value  
 Each of these functions returns a pointer to the modified template. The function returns `NULL` if `template` is badly formed or no more unique names can be created from the given template.  
  
## Remarks  
 The `_mktemp` function creates a unique file name by modifying the `template` argument. `_mktemp` automatically handles multibyte-character string arguments as appropriate, recognizing multibyte-character sequences according to the multibyte code page currently in use by the run-time system. `_wmktemp` is a wide-character version of `_mktemp`; the argument and return value of `_wmktemp` are wide-character strings. `_wmktemp` and `_mktemp` behave identically otherwise, except that `_wmktemp` does not handle multibyte-character strings.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tmktemp`|`_mktemp`|`_mktemp`|`_wmktemp`|  
  
 The `template` argument has the form `base`XXXXXX, where `base` is the part of the new file name that you supply and each X is a placeholder for a character supplied by `_mktemp`. Each placeholder character in `template` must be an uppercase X. `_mktemp` preserves `base` and replaces the first trailing X with an alphabetic character. `_mktemp` replaces the following trailing X's with a five-digit value; this value is a unique number identifying the calling process, or in multithreaded programs, the calling thread.  
  
 Each successful call to `_mktemp` modifies `template`. In each subsequent call from the same process or thread with the same `template` argument, `_mktemp` checks for file names that match names returned by `_mktemp` in previous calls. If no file exists for a given name, `_mktemp` returns that name. If files exist for all previously returned names, `_mktemp` creates a new name by replacing the alphabetic character it used in the previously returned name with the next available lowercase letter, in order, from 'a' through 'z'. For example, if `base` is:  
  
```  
fn  
```  
  
 and the five-digit value supplied by `_mktemp` is 12345, the first name returned is:  
  
```  
fna12345  
```  
  
 If this name is used to create file FNA12345 and this file still exists, the next name returned on a call from the same process or thread with the same `base` for `template` is:  
  
```  
fnb12345  
```  
  
 If FNA12345 does not exist, the next name returned is again:  
  
```  
fna12345  
```  
  
 `_mktemp` can create a maximum of 26 unique file names for any given combination of base and template values. Therefore, FNZ12345 is the last unique file name `_mktemp` can create for the `base` and `template` values used in this example.  
  
 On failure, `errno` is set. If `template` has an invalid format (for example, fewer than 6 X's), `errno` is set to `EINVAL`. If `_mktemp` is unable to create a unique name because all 26 possible file names already exist, `_mktemp` sets template to an empty string and returns `EEXIST`.  
  
 In C++, these functions have template overloads that invoke the newer, secure counterparts of these functions. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mktemp`|<io.h>|  
|`_wmktemp`|<io.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_mktemp.c  
// compile with: /W3  
/* The program uses _mktemp to create  
 * unique filenames. It opens each filename  
 * to ensure that the next name is unique.  
 */  
  
#include <io.h>  
#include <string.h>  
#include <stdio.h>  
#include <errno.h>  
  
char *template = "fnXXXXXX";  
char *result;  
char names[27][9];  
  
int main( void )  
{  
   int i;  
   FILE *fp;  
  
   for( i = 0; i < 27; i++ )  
   {  
      strcpy_s( names[i], sizeof( names[i] ), template );  
      /* Attempt to find a unique filename: */  
      result = _mktemp( names[i] );  // C4996  
      // Note: _mktemp is deprecated; consider using _mktemp_s instead  
      if( result == NULL )  
      {  
         printf( "Problem creating the template\n" );  
         if (errno == EINVAL)  
         {  
             printf( "Bad parameter\n");  
         }  
         else if (errno == EEXIST)  
         {  
             printf( "Out of unique filenames\n");   
         }  
      }  
      else  
      {  
         fopen_s( &fp, result, "w" );  
         if( fp != NULL )  
            printf( "Unique filename is %s\n", result );  
         else  
            printf( "Cannot open %s\n", result );  
         fclose( fp );  
      }  
   }  
}  
```  
  
 **Unique filename is fna03912**  
**Unique filename is fnb03912**  
**Unique filename is fnc03912**  
**Unique filename is fnd03912**  
**Unique filename is fne03912**  
**Unique filename is fnf03912**  
**Unique filename is fng03912**  
**Unique filename is fnh03912**  
**Unique filename is fni03912**  
**Unique filename is fnj03912**  
**Unique filename is fnk03912**  
**Unique filename is fnl03912**  
**Unique filename is fnm03912**  
**Unique filename is fnn03912**  
**Unique filename is fno03912**  
**Unique filename is fnp03912**  
**Unique filename is fnq03912**  
**Unique filename is fnr03912**  
**Unique filename is fns03912**  
**Unique filename is fnt03912**  
**Unique filename is fnu03912**  
**Unique filename is fnv03912**  
**Unique filename is fnw03912**  
**Unique filename is fnx03912**  
**Unique filename is fny03912**  
**Unique filename is fnz03912**  
**Problem creating the template.**  
**Out of unique filenames.**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [File Handling](../Topic/File%20Handling.md)   
 [fopen, _wfopen](../vs140/fopen--_wfopen.md)   
 [_getmbcp](../vs140/_getmbcp.md)   
 [_getpid](../vs140/_getpid.md)   
 [_open, _wopen](../Topic/_open,%20_wopen.md)   
 [_setmbcp](../vs140/_setmbcp.md)   
 [_tempnam, _wtempnam, tmpnam, _wtmpnam](../vs140/_tempnam--_wtempnam--tmpnam--_wtmpnam.md)   
 [tmpfile](../vs140/tmpfile.md)