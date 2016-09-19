---
title: "Binary Output Files"
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
ms.assetid: 180954af-8cd6-444b-9a76-2f630a3389d8
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Binary Output Files
Streams were originally designed for text, so the default output mode is text. In text mode, the newline character (hexadecimal 10) expands to a carriage return–linefeed (16-bit only). The expansion can cause problems, as shown here:  
  
```  
// binary_output_files.cpp  
// compile with: /EHsc  
#include <fstream>  
using namespace std;  
int iarray[2] = { 99, 10 };  
int main( )  
{  
    ofstream os( "test.dat" );  
    os.write( (char *) iarray, sizeof( iarray ) );  
}  
```  
  
 You might expect this program to output the byte sequence { 99, 0, 10, 0 }; instead, it outputs { 99, 0, 13, 10, 0 }, which causes problems for a program expecting binary input. If you need true binary output, in which characters are written untranslated, you could specify binary output by using the [ofstream](../vs140/ofstream.md) constructor mode argument:  
  
```  
// binary_output_files2.cpp  
// compile with: /EHsc  
#include <fstream>  
using namespace std;  
int iarray[2] = { 99, 10 };  
  
int main()  
{  
   ofstream ofs ( "test.dat", ios_base::binary );  
  
   // Exactly 8 bytes written  
   ofs.write( (char*)&iarray[0], sizeof(int)*2 );   
}  
```  
  
## See Also  
 [Output Streams](../vs140/Output-Streams.md)