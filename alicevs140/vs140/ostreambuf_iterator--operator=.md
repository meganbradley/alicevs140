---
title: "ostreambuf_iterator::operator="
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
ms.assetid: 822e5afb-0df9-45a9-8daa-39893f5997e8
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ostreambuf_iterator::operator=
The operator inserts a character into the associated stream buffer.  
  
## Syntax  
  
```  
ostreambuf_iterator<CharType, Traits>& operator=(  
   CharType _Char  
);  
```  
  
#### Parameters  
 `_Char`  
 The character to be inserted into the stream buffer.  
  
## Return Value  
 A reference to the character inserted into the stream buffer.  
  
## Remarks  
 Assignment operator used to implement the output iterator expression \**i* = *x* for writing to an output stream.  
  
## Example  
  
```  
// ostreambuf_iterator_op_assign.cpp  
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
   charOutBuf++;      // No effect on iterator position  
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