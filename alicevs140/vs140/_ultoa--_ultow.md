---
title: "_ultoa, _ultow"
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
  - _ultoa
  - _ultow
apilocation: 
  - msvcr90.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 7a472dc4-5652-4513-93c3-3358522c23be
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ultoa, _ultow
Convert an unsigned long integer to a string. More secure versions of these functions are available; see [_ultoa_s, _ultow_s](../vs140/_ultoa_s--_ultow_s.md).  
  
## Syntax  
  
```  
char *_ultoa(  
   unsigned long value,  
   char *str,  
   int radix   
);  
wchar_t *_ultow(  
   unsigned long value,  
   wchar_t *str,  
   int radix   
);  
template <size_t size>  
char *_ultoa(  
   unsigned long value,  
   char (&str)[size],  
   int radix   
); // C++ only  
template <size_t size>  
wchar_t *_ultow(  
   unsigned long value,  
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
 Base of `value`*.*  
  
## Return Value  
 Each of these functions returns a pointer to `str`. There is no error return.  
  
## Remarks  
 The `_ultoa` function converts `value` to a null-terminated character string and stores the result (up to 33 bytes) in `str`. No overflow checking is performed. `radix` specifies the base of `value`; `radix` must be in the range 2 – 36. `_ultow` is a wide-character version of `_ultoa`.  
  
> [!IMPORTANT]
>  To prevent buffer overruns, ensure that the `str` buffer is large enough to hold the converted digits plus the trailing null-character.  
  
 In C++, these functions have template overloads that invoke the newer, secure counterparts of these functions. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_ultot`|`_ultoa`|`_ultoa`|`_ultow`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_ultoa`|<stdlib.h>|  
|`_ultow`|<stdlib.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [_itoa](../vs140/_itoa--_i64toa--_ui64toa--_itow--_i64tow--_ui64tow.md).  
  
## .NET Framework Equivalent  
 [System::Convert::ToString](https://msdn.microsoft.com/en-us/library/system.convert.tostring.aspx)  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [_itoa, _i64toa, _ui64toa, _itow, _i64tow, _ui64tow](../vs140/_itoa--_i64toa--_ui64toa--_itow--_i64tow--_ui64tow.md)