---
title: "cerr"
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
ms.assetid: 3e9f0d43-c801-41c0-b17b-4d8b62f31178
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# cerr
The object `cerr` controls output to a stream buffer associated with the object `stderr`, declared in <cstdio\>.  
  
## Syntax  
  
```  
extern ostream cerr;  
```  
  
## Return Value  
 An [ostream](../vs140/ostream.md) object.  
  
## Remarks  
 The object controls unbuffered insertions to the standard error output as a byte stream. Once the object is constructed, the expression `cerr.`[flags](../vs140/ios_base--flags.md) `&` [unitbuf](../vs140/unitbuf.md) is nonzero, and `cerr.tie() == &cout`.  
  
## Example  
  
```  
// iostream_cerr.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
using namespace std;  
  
void TestWide( )   
{  
   int i = 0;  
   wcout << L"Enter a number: ";  
   wcin >> i;  
   wcerr << L"test for wcerr" << endl;  
   wclog << L"test for wclog" << endl;     
}  
  
int main( )   
{  
   int i = 0;  
   cout << "Enter a number: ";  
   cin >> i;  
   cerr << "test for cerr" << endl;  
   clog << "test for clog" << endl;  
   TestWide( );  
}  
```  
  
## Input  
  
```  
3  
1  
```  
  
## Sample Output  
  
```  
Enter a number: 3  
test for cerr  
test for clog  
Enter a number: 1  
test for wcerr  
test for wclog  
```  
  
## Requirements  
 **Header:** <iostream\>  
  
 **Namespace:** std  
  
## See Also  
 [ostream](../vs140/ostream.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)