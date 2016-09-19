---
title: "Storage of Addresses"
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
ms.assetid: 423b2402-b847-4788-ad70-943b7c9c5c8b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Storage of Addresses
The amount of storage required for an address and the meaning of the address depend on the implementation of the compiler. Pointers to different types are not guaranteed to have the same length. Therefore, **sizeof(char \*)** is not necessarily equal to **sizeof(int \*)**.  
  
 **Microsoft Specific**  
  
 For the Microsoft C compiler, **sizeof(char \*)** is equal to **sizeof(int \*)**.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Pointer Declarations](../vs140/Pointer-Declarations.md)