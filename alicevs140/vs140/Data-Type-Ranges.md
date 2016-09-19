---
title: "Data Type Ranges"
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
ms.assetid: 3691ceca-05fb-4b82-b1ae-5c4618cda91a
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Type Ranges
Visual C++ 32-bit and 64-bit compilers recognize the types in the table later in this article.  
  
-   `int` (`unsigned``int`)  
  
-   `__int8` (`unsigned``__int8`)  
  
-   `__int16` (`unsigned``__int16`)  
  
-   `__int32` (`unsigned``__int32`)  
  
-   `__int64` (`unsigned``__int64`)  
  
-   `short` (`unsigned``short`)  
  
-   `long` (`unsigned``long`)  
  
-   `long` `long` (`unsigned``long``long`)  
  
 If its name begins with two underscores (`__`), a data type is non-standard.  
  
 The ranges that are specified in the following table are inclusive-inclusive.  
  
|Type Name|Bytes|Other Names|Range of Values|  
|---------------|-----------|-----------------|---------------------|  
|int|4|signed|–2,147,483,648 to 2,147,483,647|  
|unsigned int|4|unsigned|0 to 4,294,967,295|  
|__int8|1|char|–128 to 127|  
|unsigned __int8|1|unsigned char|0 to 255|  
|__int16|2|short, short int, signed short int|–32,768 to 32,767|  
|unsigned __int16|2|unsigned short, unsigned short int|0 to 65,535|  
|__int32|4|signed, signed int, int|–2,147,483,648 to 2,147,483,647|  
|unsigned __int32|4|unsigned, unsigned int|0 to 4,294,967,295|  
|__int64|8|long long, signed long long|–9,223,372,036,854,775,808 to 9,223,372,036,854,775,807|  
|unsigned __int64|8|unsigned long long|0 to 18,446,744,073,709,551,615|  
|bool|1|none|false or true|  
|char|1|none|–128 to 127 by default<br /><br /> 0 to 255 when compiled by using [/J](../vs140/-J--Default-char-Type-Is-unsigned-.md)|  
|signed char|1|none|–128 to 127|  
|unsigned char|1|none|0 to 255|  
|short|2|short int, signed short int|–32,768 to 32,767|  
|unsigned short|2|unsigned short int|0 to 65,535|  
|long|4|long int, signed long int|–2,147,483,648 to 2,147,483,647|  
|unsigned long|4|unsigned long int|0 to 4,294,967,295|  
|long long|8|none (but equivalent to __int64)|–9,223,372,036,854,775,808 to 9,223,372,036,854,775,807|  
|unsigned long long|8|none (but equivalent to unsigned __int64)|0 to 18,446,744,073,709,551,615|  
|enum|varies|none|See [Remarks](#bkmkRemarks) later in this article|  
|float|4|none|3.4E +/- 38 (7 digits)|  
|double|8|none|1.7E +/- 308 (15 digits)|  
|long double|same as double|none|Same as double|  
|wchar_t|2|__wchar_t|0 to 65,535|  
  
 Depending on how it's used, a variable of `__wchar_t` designates either a wide-character type or multibyte-character type. Use the `L` prefix before a character or string constant to designate the wide-character-type constant.  
  
 `signed` and `unsigned` are modifiers that you can use with any integral type except `bool`. Note that `char`, `signed char`, and `unsigned char` are three distinct types for the purposes of mechanisms like overloading and templates.  
  
 The `int` and `unsigned``int` types have a size of four bytes. However, portable code should not depend on the size of `int` because the language standard allows this to be implementation-specific.  
  
 C/C++ in Visual Studio also supports sized integer types. For more information, see [__int8, \__int16, \__int32, \__int64](../vs140/__int8--__int16--__int32--__int64.md) and [Integer Limits](../vs140/Integer-Limits.md).  
  
 For more information about the restrictions of the sizes of each type, see [Fundamental Types](../vs140/Fundamental-Types---C---.md).  
  
 The range of enumerated types varies depending on the language context and specified compiler flags. For more information, see [C Enumeration Declarations](../vs140/C-Enumeration-Declarations.md) and [C++ Enumeration Declarations](../vs140/Enumerations--C---.md).  
  
## See Also  
 [Keywords](../vs140/Keywords--C---.md)   
 [Fundamental Types](../vs140/Fundamental-Types---C---.md)