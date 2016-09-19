---
title: "codecvt_mode"
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
ms.assetid: c5dccee5-6fb7-4dbe-8dbc-b261f4c17b2f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# codecvt_mode
Specifies configuration information for [locale](../vs140/locale-Class.md) facets.  
  
## Syntax  
  
```  
enum codecvt_mode {  
    consume_header = 4,  
    generate_header = 2,  
    little_endian = 1  
    };  
```  
  
## Remarks  
 The enumeration defines three constants that supply configuration information to the locale facets declared in [<codecvt\>](../vs140/-codecvt-.md). The distinct values are:  
  
-   `consume_header`, to consume an initial header sequence when reading a multibyte sequence and determine the endianness of the subsequent multibyte sequence to be read  
  
-   `generate_header`, to generate an initial header sequence when writing a multibyte sequence to advertise the endianness of the subsequent multibyte sequence to be written  
  
-   `little_endian`, to generate a multibyte sequence in little-endian order, as opposed to the default big-endian order  
  
 These constants can be ORed together in arbitrary combinations.  
  
## Requirements  
 **Header:** <codecvt\>  
  
 **Namespace:** std