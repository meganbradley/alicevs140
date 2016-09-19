---
title: "ifstream"
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
ms.assetid: e51677b3-ecba-4eef-a4b0-bb6232eabd81
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ifstream
Defines a stream to be used to read single-byte character data serially from a file. `ifstream` is a typedef that specializes the template class `basic_ifstream` for `char`.  
  
 There is also `wifstream`, a typedef that specializes `basic_ifstream` to read `wchar_t` double-wide characters. For more information, see [wifstream](../vs140/wifstream.md).  
  
## Syntax  
  
```  
typedef basic_ifstream<char, char_traits<char> > ifstream;  
```  
  
## Remarks  
 The type is a synonym for template class `basic_ifstream`, specialized for elements of type char with default character traits. An example is  
  
 `using namespace std;`  
  
 `ifstream infile("existingtextfile.txt");`  
  
 `if (!infile.bad())`  
  
 `{`  
  
 `// Dump the contents of the file to cout.`  
  
 `cout << infile.rdbuf();`  
  
 `infile.close();`  
  
 `}`  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ifstream Class](../vs140/basic_ifstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)