---
title: "bitset::to_ullong"
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
ms.assetid: e34ec092-741a-4a79-97d6-b4d9c0774c0a
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bitset::to_ullong
Returns an unsigned long long value that contains the same bits set as the contents of the bitset object.  
  
## Syntax  
  
```  
unsigned long long to_ullong() const;  
```  
  
#### Parameters  
  
## Property Value/Return Value  
 Returns the sum of the bit values that are in the bit sequence as an unsigned long long. This unsigned long long value would re-create the same set bits if it is used to initialize a bitset.  
  
## Exceptions  
 The method throws an [overflow_error](../vs140/overflow_error-Class.md) if any bit in the bit sequence has a bit value that cannot be represented as a value of type `unsigned long long`.  
  
## Remarks  
 Returns the sum of the bit values in the bit sequence as an unsigned long long.  
  
## Requirements  
 **Header:** <bitset\>  
  
 **Namespace:** std  
  
## See Also  
 [bitset Class](../vs140/bitset-Class.md)   
 [<bitset\>](../vs140/-bitset-.md)