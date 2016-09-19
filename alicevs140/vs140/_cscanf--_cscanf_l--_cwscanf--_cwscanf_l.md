---
title: "_cscanf, _cscanf_l, _cwscanf, _cwscanf_l"
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
  - _cscanf_l
  - _cscanf
  - _cwscanf
  - _cwscanf_l
apilocation: 
  - msvcr90.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: dbfe7547-b577-4567-a1cb-893fa640e669
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _cscanf, _cscanf_l, _cwscanf, _cwscanf_l
Reads formatted data from the console. More secure versions of these functions are available; see [_cscanf_s, _cscanf_s_l, _cwscanf_s, _cwscanf_s_l](../vs140/_cscanf_s--_cscanf_s_l--_cwscanf_s--_cwscanf_s_l.md).  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _cscanf(   
   const char *format [,  
   argument] ...   
);  
int _cscanf_l(   
   const char *format,  
   locale_t locale [,  
   argument] ...   
);  
int _cwscanf(   
   const wchar_t *format [,  
   argument] ...   
);  
int _cwscanf_l(   
   const wchar_t *format,  
   locale_t locale [,  
   argument] ...   
);  
```  
  
#### Parameters  
 `format`  
 Format-control string.  
  
 `argument`  
 Optional parameters.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 The number of fields that were successfully converted and assigned. The return value does not include fields that were read but not assigned. The return value is `EOF` for an attempt to read at end of file. This can occur when keyboard input is redirected at the operating-system command-line level. A return value of 0 means that no fields were assigned.  
  
## Remarks  
 The `_cscanf` function reads data directly from the console into the locations given by `argument`. The [_getche](../vs140/_getch--_getwch.md) function is used to read characters. Each optional parameter must be a pointer to a variable with a type that corresponds to a type specifier in `format`. The format controls the interpretation of the input fields and has the same form and function as the `format` parameter for the [scanf](../vs140/scanf--_scanf_l--wscanf--_wscanf_l.md) function. While `_cscanf` normally echoes the input character, it does not do so if the last call was to `_ungetch`.  
  
 This function validates its parameters. If format is NULL, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and the function returns `EOF`.  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tcscanf`|`_cscanf`|`_cscanf`|`_cwscanf`|  
|`_tcscanf_l`|`_cscanf_l`|`_cscanf_l`|`_cwscanf_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_cscanf`,`_cscanf_l`|<conio.h>|  
|`_cwscanf`, `_cwscanf_l`|<conio.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_cscanf.c  
// compile with: /c /W3  
/* This program prompts for a string  
 * and uses _cscanf to read in the response.  
 * Then _cscanf returns the number of items  
 * matched, and the program displays that number.  
 */  
  
#include <stdio.h>  
#include <conio.h>  
  
int main( void )  
{  
   int   result, i[3];  
  
   _cprintf_s( "Enter three integers: ");  
   result = _cscanf( "%i %i %i", &i[0], &i[1], &i[2] ); // C4996  
   // Note: _cscanf is deprecated; consider using _cscanf_s instead  
   _cprintf_s( "\r\nYou entered " );  
   while( result-- )  
      _cprintf_s( "%i ", i[result] );  
   _cprintf_s( "\r\n" );  
}  
```  
  
## Input  
  
```  
1 2 3  
```  
  
## Output  
  
```  
Enter three integers: 1 2 3  
You entered 3 2 1  
```  
  
## See Also  
 [Console and Port I/O](../vs140/Console-and-Port-I-O.md)   
 [_cprintf, _cwprintf](../vs140/_cprintf--_cprintf_l--_cwprintf--_cwprintf_l.md)   
 [fscanf, fwscanf](../vs140/fscanf--_fscanf_l--fwscanf--_fwscanf_l.md)   
 [scanf_s, wscanf_s](../vs140/scanf_s--_scanf_s_l--wscanf_s--_wscanf_s_l.md)   
 [sscanf, swscanf](../vs140/sscanf--_sscanf_l--swscanf--_swscanf_l.md)