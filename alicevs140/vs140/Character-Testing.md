---
title: "Character Testing"
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
ms.assetid: 376ba061-bae3-427e-9569-33fa5949a199
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Character Testing
**ANSI 4.3.1** The sets of characters tested for by the `isalnum`, `isalpha`, `iscntrl`, `islower`, `isprint`, and `isupper` functions  
  
 The following list describes these functions as they are implemented by the Microsoft C compiler.  
  
|Function|Tests For|  
|--------------|---------------|  
|`isalnum`|Characters 0 – 9, A–Z, a–z ASCII 48–57, 65–90, 97–122|  
|`isalpha`|Characters A–Z, a–z ASCII 65–90, 97–122|  
|`iscntrl`|ASCII 0 –31, 127|  
|`islower`|Characters a–z ASCII 97–122|  
|`isprint`|Characters A–Z, a–z, 0 – 9, punctuation, space ASCII 32–126|  
|`isupper`|Characters A–Z ASCII 65–90|  
  
## See Also  
 [Library Functions](../vs140/Library-Functions.md)