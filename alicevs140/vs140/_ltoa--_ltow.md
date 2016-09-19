---
title: "_ltoa, _ltow"
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
  - _ltoa
  - _ltow
apilocation: 
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 14036104-2c25-4759-87c0-918ed8521e47
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ltoa, _ltow
Converts a long integer to a string. More secure versions of these functions are available; see [_ltoa_s, _ltow_s](../vs140/_ltoa_s--_ltow_s.md).  
  
## Syntax  
  
```  
char *_ltoa(  
   long value,  
   char *str,  
   int radix   
);  
wchar_t *_ltow(  
   long value,  
   wchar_t *str,  
   int radix   
);  
template <size_t size>  
char *_ltoa(  
   long value,  
   char (&str)[size],  
   int radix   
); // C++ only  
template <size_t size>  
wchar_t *_ltow(  
   long value,  
   wchar_t (&str)[size],  
   int radix   
); // C++ only  
```  
  
#### Parameters  
 `value`  
 Number to be converted.  
  
 `str`  
 String result.  
  
 `radix`  
 Base of `value`.  
  
## Return Value  
 Each of these functions returns a pointer to `str`. There is no error return.  
  
## Remarks  
 The `_ltoa` function converts the digits of `value` to a null-terminated character string and stores the result (up to 33 bytes) in `str`. The `radix` argument specifies the base of `value`, which must be in the range 2 – 36. If `radix` equals 10 and `value` is negative, the first character of the stored string is the minus sign (–). `_ltow` is a wide-character version of `_ltoa`; the second argument and return value of `_ltow` are wide-character strings. Each of these functions is Microsoft-specific.  
  
> [!IMPORTANT]
>  To prevent buffer overruns, ensure that the `str` buffer is large enough to hold the converted digits plus the trailing null-character and a sign character.  
  
 In C++, these functions have template overloads. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_ltot`|`_ltoa`|`_ltoa`|`_ltow`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_ltoa`|<stdlib.h>|  
|`_ltow`|<stdlib.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [_itoa](../vs140/_itoa--_i64toa--_ui64toa--_itow--_i64tow--_ui64tow.md).  
  
## .NET Framework Equivalent  
 [System::Convert::ToString](https://msdn.microsoft.com/en-us/library/system.convert.tostring.aspx)  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [_itoa, _i64toa, _ui64toa, _itow, _i64tow, _ui64tow](../vs140/_itoa--_i64toa--_ui64toa--_itow--_i64tow--_ui64tow.md)   
 [_ultoa, _ultow](../vs140/_ultoa--_ultow.md)