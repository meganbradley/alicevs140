---
title: "ostream_iterator::operator*"
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
ms.assetid: 8ac7bd2f-23ae-446d-a94d-8efca1a2264d
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ostream_iterator::operator*
Dereferencing operator used to implement the output iterator expression \**ii* = *x*.  
  
## Syntax  
  
```  
  
ostream_iterator<Type, CharType, Traits>& operator*( );  
  
```  
  
## Return Value  
 A reference to the `ostream_iterator`.  
  
## Remarks  
 The requirements for an output iterator that the `ostream_iterator` must satisfy require only the expression \**ii* = *t* be valid and says nothing about the **operator** or the `operator=` on their own. The member operator in this implementation returns **\*this**.  
  
## Example  
  
```  
// ostream_iterator_op_deref.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   // ostream_iterator for stream cout  
   // with new line delimiter  
   ostream_iterator<int> intOut ( cout , "\n" );  
  
   // Standard iterator interface for writing  
   // elements to the output stream  
   cout << "Elements written to output stream:" << endl;  
   *intOut = 10;  
   intOut++;      // No effect on iterator position  
   *intOut = 20;  
   *intOut = 30;  
}  
```  
  
 **Elements written to output stream:**  
**10**  
**20**  
**30**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [ostream_iterator Class](../vs140/ostream_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)