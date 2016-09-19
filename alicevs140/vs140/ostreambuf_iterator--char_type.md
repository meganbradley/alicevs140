---
title: "ostreambuf_iterator::char_type"
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
ms.assetid: 02a1869b-f5ea-4df0-bab9-ec63c7a040af
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ostreambuf_iterator::char_type
A type that provides for the character type of the `ostreambuf_iterator`.  
  
## Syntax  
  
```  
  
typedef CharType char_type;  
  
```  
  
## Remarks  
 The type is a synonym for the template parameter **CharType**.  
  
## Example  
  
```  
// ostreambuf_iterator_char_type.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <vector>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
  
   typedef ostreambuf_iterator<char>::char_type CHT1;  
   typedef ostreambuf_iterator<char>::traits_type CHTR1;  
  
   // ostreambuf_iterator for stream cout  
   // with new line delimiter:  
    ostreambuf_iterator< CHT1, CHTR1> charOutBuf ( cout );  
  
   // Standard iterator interface for writing  
   // elements to the output streambuf:  
   cout << "The characters written to the output stream\n"  
        << " by charOutBuf are: ";  
   *charOutBuf = 'O';  
   charOutBuf++;  
   *charOutBuf = 'U';  
   charOutBuf++;  
   *charOutBuf = 'T';  
   charOutBuf++;  
   cout << "." << endl;  
}  
```  
  
 **The characters written to the output stream**  
 **by charOutBuf are: OUT.**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [ostreambuf_iterator Class](../vs140/ostreambuf_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)