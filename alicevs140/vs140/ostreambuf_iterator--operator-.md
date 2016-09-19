---
title: "ostreambuf_iterator::operator*"
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
ms.assetid: 54b8073b-7071-4825-8c83-f7a0b7a7f1a4
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ostreambuf_iterator::operator*
A nonfunctional dereferencing operator used to implement the output iterator expression \**i* = *x*.  
  
## Syntax  
  
```  
ostreambuf_iterator<CharType, Traits>& operator*( );  
```  
  
## Return Value  
 The ostreambuf iterator object.  
  
## Remarks  
 This operator functions only in the output iterator expression \**i* = *x* to output characters to stream buffer. Applied to an ostreambuf iterator, it returns the iterator; **\*iter** returns **iter**,  
  
## Example  
  
```  
// ostreambuf_iterator_op_deref.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   // ostreambuf_iterator for stream cout  
   // with new line delimiter  
   ostreambuf_iterator<char> charOutBuf ( cout );  
  
   // Standard iterator interface for writing  
   // elements to the output stream  
   cout << "Elements written to output stream:" << endl;  
   *charOutBuf = 'O';  
   charOutBuf++;   // no effect on iterator position  
   *charOutBuf = 'U';  
   *charOutBuf = 'T';  
}  
```  
  
 **Elements written to output stream:**  
**OUT**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [ostreambuf_iterator Class](../vs140/ostreambuf_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)