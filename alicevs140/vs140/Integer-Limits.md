---
title: "Integer Limits"
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
ms.assetid: 6922bdbf-0f49-443b-bc03-ee182e4cbd57
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Integer Limits
**Microsoft Specific**  
  
 The limits for integer types are listed in the following table. These limits are also defined in the standard header file LIMITS.H.  
  
### Limits on Integer Constants  
  
|Constant|Meaning|Value|  
|--------------|-------------|-----------|  
|**CHAR_BIT**|Number of bits in the smallest variable that is not a bit field.|8|  
|**SCHAR_MIN**|Minimum value for a variable of type **signed char**.|–128|  
|**SCHAR_MAX**|Maximum value for a variable of type **signed char**.|127|  
|**UCHAR_MAX**|Maximum value for a variable of type `unsigned char`.|255 (0xff)|  
|**CHAR_MIN**|Minimum value for a variable of type `char`.|–128; 0 if /J option used|  
|**CHAR_MAX**|Maximum value for a variable of type `char`.|127; 255 if /J option used|  
|**MB_LEN_MAX**|Maximum number of bytes in a multicharacter constant.|5|  
|**SHRT_MIN**|Minimum value for a variable of type **short**.|–32768|  
|**SHRT_MAX**|Maximum value for a variable of type **short**.|32767|  
|**USHRT_MAX**|Maximum value for a variable of type **unsigned short**.|65535 (0xffff)|  
|**INT_MIN**|Minimum value for a variable of type `int`.|–2147483648|  
|**INT_MAX**|Maximum value for a variable of type `int`.|2147483647|  
|**UINT_MAX**|Maximum value for a variable of type `unsigned int`.|4294967295 (0xffffffff)|  
|**LONG_MIN**|Minimum value for a variable of type **long**.|–2147483648|  
|**LONG_MAX**|Maximum value for a variable of type **long**.|2147483647|  
|**ULONG_MAX**|Maximum value for a variable of type `unsigned long`.|4294967295 (0xffffffff)|  
|**_I64_MIN**|Minimum value for a variable of type `__int64`|-9223372036854775808|  
|**_I64_MAX**|Maximum value for a variable of type `__int64`|9223372036854775807|  
|**_UI64_MAX**|Maximum value for a variable of type **unsigned __int64**|18446744073709551615 (0xffffffffffffffff)|  
  
 If a value exceeds the largest integer representation, the Microsoft compiler generates an error.  
  
## END Microsoft Specific  
  
## See Also  
 [Floating Limits](../vs140/Floating-Limits.md)