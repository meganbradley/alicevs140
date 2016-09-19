---
title: "_mbsnbicmp, _mbsnbicmp_l"
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
  - _mbsnbicmp_l
  - _mbsnbicmp
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: ddb44974-8b0c-42f0-90d0-56c9350bae0c
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mbsnbicmp, _mbsnbicmp_l
Compares `n` bytes of two multibyte-character strings, and ignores case.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _mbsnbicmp(  
   const unsigned char *string1,  
   const unsigned char *string2,  
   size_t count   
);  
```  
  
#### Parameters  
 `string1, string2`  
 Null-terminated strings to compare.  
  
 `count`  
 Number of bytes to compare.  
  
## Return Value  
 The return value indicates the relationship between the substrings.  
  
|Return value|Description|  
|------------------|-----------------|  
|< 0|`string1` substring less than `string2` substring.|  
|0|`string1` substring identical to `string2` substring.|  
|> 0|`string1` substring greater than `string2` substring.|  
  
 On an error, `_mbsnbcmp` returns `_NLSCMPERROR`, which is defined in String.h and Mbstring.h.  
  
## Remarks  
 The `_mbsnbicmp` function performs an ordinal comparison of at most the first `count` bytes of `string1` and `string2`. The comparison is performed by converting each character to lowercase; `_mbsnbcmp` is a case-sensitive version of `_mbsnbicmp`. The comparison ends if a terminating null character is reached in either string before `count` characters are compared. If the strings are equal when a terminating null character is reached in either string before `count` characters are compared, the shorter string is lesser.  
  
 `_mbsnbicmp`  is similar to `_mbsnicmp`, except that it compares strings up to `count` bytes instead of by characters.  
  
 Two strings containing characters located between 'Z' and 'a' in the ASCII table ('[', '\\', ']', '^', '_', and '\`') compare differently, depending on their case. For example, the two strings "`ABCDE`" and "`ABCD^`" compare one way if the comparison is lowercase ("`abcde`" > "`abcd^`") and the other way ("`ABCDE`" < "`ABCD^`") if it is uppercase.  
  
 `_mbsnbicmp` recognizes multibyte-character sequences according to the [multibyte code page](../vs140/Code-Pages.md) currently in use. It is not affected by the current locale setting.  
  
 If either `string1` or `string2` is a null pointer, `_mbsnbicmp` invokes the invalid parameter handler as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the function returns `_NLSCMPERROR` and sets `errno` to `EINVAL`.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tcsnicmp`|`_strnicmp`|`_mbsnbicmp`|`_wcsnicmp`|  
|`_tcsnicmp_l`|`_strnicmp_l`|`_mbsnbicmp_l`|`_wcsnicmp_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbsnbicmp`|<mbstring.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
 See the example for [_mbsnbcmp, _mbsnbcmp_l](../vs140/_mbsnbcmp--_mbsnbcmp_l.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [_mbsnbcat, _mbsnbcat_l](../vs140/_mbsnbcat--_mbsnbcat_l.md)   
 [_mbsnbcmp, _mbsnbcmp_l](../vs140/_mbsnbcmp--_mbsnbcmp_l.md)   
 [_stricmp, _wcsicmp, _mbsicmp, _stricmp_l, _wcsicmp_l, _mbsicmp_l](../vs140/_stricmp--_wcsicmp--_mbsicmp--_stricmp_l--_wcsicmp_l--_mbsicmp_l.md)