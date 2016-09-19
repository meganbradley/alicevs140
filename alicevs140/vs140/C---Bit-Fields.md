---
title: "C++ Bit Fields"
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
ms.topic: article
ms.assetid: 6f4b62e3-cc1d-4e5d-bf34-05904104f71a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C++ Bit Fields
Classes and structures can contain members that occupy less storage than an integral type. These members are specified as bit fields. The syntax for bit-field *member-declarator* specification follows:  
  
## Syntax  
  
```  
  
declarator  : constant-expression  
```  
  
## Remarks  
 The (optional) `declarator` is the name by which the member is accessed in the program. It must be an integral type (including enumerated types). The *constant-expression* specifies the number of bits the member occupies in the structure. Anonymous bit fields — that is, bit-field members with no identifier — can be used for padding.  
  
> [!NOTE]
>  An unnamed bit field of width 0 forces alignment of the next bit field to the next `type` boundary, where `type` is the type of the member.  
  
 The following example declares a structure that contains bit fields:  
  
```  
// bit_fields1.cpp  
// compile with: /LD  
struct Date {  
   unsigned short nWeekDay  : 3;    // 0..7   (3 bits)  
   unsigned short nMonthDay : 6;    // 0..31  (6 bits)  
   unsigned short nMonth    : 5;    // 0..12  (5 bits)  
   unsigned short nYear     : 8;    // 0..100 (8 bits)  
};  
```  
  
 The conceptual memory layout of an object of type `Date` is shown in the following figure.  
  
 ![Memory layout of a date object](../vs140/media/vc38UQ1.png "vc38UQ1")  
Memory Layout of Date Object  
  
 Note that `nYear` is 8 bits long and would overflow the word boundary of the declared type, **unsigned short**. Therefore, it is begun at the beginning of a new **unsigned short**. It is not necessary that all bit fields fit in one object of the underlying type; new units of storage are allocated, according to the number of bits requested in the declaration.  
  
 **Microsoft Specific**  
  
 The ordering of data declared as bit fields is from low to high bit, as shown in the figure above.  
  
 **END Microsoft Specific**  
  
 If the declaration of a structure includes an unnamed field of length 0, as shown in the following example,  
  
```  
// bit_fields2.cpp  
// compile with: /LD  
struct Date {  
   unsigned nWeekDay  : 3;    // 0..7   (3 bits)  
   unsigned nMonthDay : 6;    // 0..31  (6 bits)  
   unsigned           : 0;    // Force alignment to next boundary.  
   unsigned nMonth    : 5;    // 0..12  (5 bits)  
   unsigned nYear     : 8;    // 0..100 (8 bits)  
};  
```  
  
 the memory layout is as shown in the following figure.  
  
 ![Layout of Date object with zero&#45;length bit field](../vs140/media/vc38UQ2.png "vc38UQ2")  
Layout of Date Object with Zero-Length Bit Field  
  
 The underlying type of a bit field must be an integral type, as described in [Fundamental Types](../vs140/Fundamental-Types---C---.md).  
  
## Restrictions on bit fields  
 The following list details erroneous operations on bit fields:  
  
1.  Taking the address of a bit field.  
  
2.  Initializing a reference with a bit field.  
  
## See Also  
 [Classes and Structs](../vs140/Classes-and-Structs--C---.md)