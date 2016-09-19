---
title: "ostream_iterator::char_type"
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
ms.assetid: 20675077-0ae1-47ad-a67f-c49b5358d6b4
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# ostream_iterator::char_type
A type that provides for the character type of the iterator.  
  
## Syntax  
  
```  
  
typedef CharType char_type;  
  
```  
  
## Remarks  
 The type is a synonym for the template parameter **CharType**.  
  
## Example  
  
```  
// ostream_iterator_char_type.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   typedef ostream_iterator<int>::char_type CHT1;  
   typedef ostream_iterator<int>::traits_type CHTR1;  
  
   // ostream_iterator for stream cout  
   // with new line delimiter:  
    ostream_iterator<int, CHT1, CHTR1> intOut ( cout , "\n" );  
  
   // Standard iterator interface for writing  
   // elements to the output stream:  
   cout << "The integers written to the output stream\n"  
        << "by intOut are:" << endl;  
   *intOut = 10;  
   *intOut = 20;  
   *intOut = 30;  
}  
```  
  
 **The integers written to the output stream**  
**by intOut are:**  
**10**  
**20**  
**30**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [ostream_iterator Class](../vs140/ostream_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)