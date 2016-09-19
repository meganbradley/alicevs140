---
title: "C++ Integer Limits"
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
ms.assetid: 0c23cbd6-29fb-4d9c-b689-5984e19748de
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C++ Integer Limits
**Microsoft Specific**  
  
 The limits for integer types are listed in the following table. These limits are defined in the standard header file LIMITS.H. Microsoft C also permits the declaration of sized integer variables, which are integral types of size 8-, 16-, or 32-bits. For more information on sized integers, see [Sized Integer Types](../vs140/C-Sized-Integer-Types.md).  
  
### Limits on Integer Constants  
  
|**Constant**|Meaning|Value|  
|------------------|-------------|-----------|  
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
|**INT_MIN**|Minimum value for a variable of type `int`.|–2147483647 – 1|  
|**INT_MAX**|Maximum value for a variable of type `int`.|2147483647|  
|**UINT_MAX**|Maximum value for a variable of type `unsigned int`.|4294967295 (0xffffffff)|  
|**LONG_MIN**|Minimum value for a variable of type **long**.|–2147483647 – 1|  
|**LONG_MAX**|Maximum value for a variable of type **long**.|2147483647|  
|**ULONG_MAX**|Maximum value for a variable of type `unsigned long`.|4294967295 (0xffffffff)|  
  
 If a value exceeds the largest integer representation, the Microsoft compiler generates an error.  
  
 **END Microsoft Specific**  
  
## See Also  
 [C Integer Constants](../vs140/C-Integer-Constants.md)