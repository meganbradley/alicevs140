---
title: "operator^ (&lt;bitset&gt;)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e5fc14ea-11c5-4043-ad7d-1960fea10b0d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator^ (&lt;bitset&gt;)
Performs a bitwise `EXCLUSIVE-OR` between two bitsets.  
  
## Syntax  
  
```  
template <size_t size>  
bitset<size> operator^(  
   const bitset<size>& _Left,  
   const bitset<size>& _Right  
);  
```  
  
#### Parameters  
 `_Left`  
 The first of the two bitsets whose respective elements are to be combined with the bitwise `EXCLUSIVE-OR`.  
  
 `_Right`  
 The second of the two valarrays whose respective elements are to be combined with the bitwise `EXCLUSIVE-OR`.  
  
## Return Value  
 A bitset whose elements are the result of performing the `EXCLUSIVE-OR` operation on the corresponding elements of `_Left` and `_Right`.  
  
## Example  
  
```  
// bitset_xor.cpp  
// compile with: /EHsc  
#include <bitset>  
#include <iostream>  
#include <string>  
  
using namespace std;  
  
int main()  
{  
   bitset<4> b1 ( string("0101") );  
   bitset<4> b2 ( string("0011") );  
   bitset<4> b3 = b1 ^ b2;  
   cout << "bitset 1: " << b1 << endl;  
   cout << "bitset 2: " << b2 << endl;  
   cout << "bitset 3: " << b3 << endl;  
}  
```  
  
 **bitset 1: 0101**  
**bitset 2: 0011**  
**bitset 3: 0110**   
## Requirements  
 **Header:** <bitset\>  
  
 **Namespace:** std