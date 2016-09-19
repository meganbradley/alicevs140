---
title: "Type int"
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
ms.assetid: 0067ce9a-281e-491a-ae63-632952981e13
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type int
The size of a signed or unsigned `int` item is the standard size of an integer on a particular machine. For example, in 16-bit operating systems, the `int` type is usually 16 bits, or 2 bytes. In 32-bit operating systems, the `int` type is usually 32 bits, or 4 bytes. Thus, the `int` type is equivalent to either the `short int` or the **long int** type, and the `unsigned int` type is equivalent to either the **unsigned short** or the `unsigned long` type, depending on the target environment. The `int` types all represent signed values unless specified otherwise.  
  
 The type specifiers `int` and `unsigned int` (or simply `unsigned`) define certain features of the C language (for instance, the `enum` type). In these cases, the definitions of `int` and unsigned int for a particular implementation determine the actual storage.  
  
 **Microsoft Specific**  
  
 Signed integers are represented in two's-complement form. The most-significant bit holds the sign: 1 for negative, 0 for positive and zero. The range of values is given in [C Integer Limits](../vs140/C---Integer-Limits.md), which is taken from the LIMITS.H header file.  
  
 **END Microsoft Specific**  
  
> [!NOTE]
>  The int and unsigned int type specifiers are widely used in C programs because they allow a particular machine to handle integer values in the most efficient way for that machine. However, since the sizes of the int and unsigned int types vary, programs that depend on a specific int size may not be portable to other machines. To make programs more portable, you can use expressions with the sizeof operator (as discussed in [The sizeof Operator](../vs140/sizeof-Operator--C-.md)) instead of hard-coded data sizes.  
  
## See Also  
 [Storage of Basic Types](../vs140/Storage-of-Basic-Types.md)