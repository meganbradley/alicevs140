---
title: "basic_streambuf::sputn"
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
ms.assetid: c5e3f1ae-ab89-4cc4-9c9f-f467c541c25c
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::sputn
Puts a character string into the stream.  
  
## Syntax  
  
```  
  
      streamsize sputn(  
   const char_type *_Ptr,  
   streamsize _Count  
);  
```  
  
#### Parameters  
 `_Ptr`  
 The character string.  
  
 `_Count`  
 The count of characters.  
  
## Return Value  
 The number of characters actually inserted into the stream.  
  
## Remarks  
 The member function returns [xsputn](../vs140/basic_streambuf--xsputn.md)(`_Ptr`, `_Count`). See the Remarks section of this member for more information.  
  
## Example  
  
```  
// basic_streambuf_sputn.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main()  
{  
    using namespace std;  
  
    streamsize i = cout.rdbuf()->sputn("test", 4);  
    cout << endl << i << endl;  
}  
```  
  
 **test**  
**4**   
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)