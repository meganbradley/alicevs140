---
title: "basic_filebuf::setbuf"
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
ms.assetid: 124c7ab2-33c2-4490-89cc-20b326080caf
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_filebuf::setbuf
Performs an operation particular to each derived stream buffer.  
  
## Syntax  
  
```  
virtual basic_streambuf<Elem, Tr> *setbuf(  
    char_type *_Buffer,  
    streamsize _Count  
);  
```  
  
#### Parameters  
 `_Buffer`  
 Pointer to a buffer.  
  
 `_Count`  
 Size of the buffer.  
  
## Return Value  
 The protected member function returns zero if the file pointer `fp` is a null pointer.  
  
## Remarks  
 `setbuf` calls `setvbuf`(**fp**, (`char` \*)`_Buffer`, `_IOFBF`, `_Count` \* `sizeof` (**Elem**) ) to offer the array of `_Count` elements beginning at _*Buffer* as a buffer for the stream. If that function returns a nonzero value, the function returns a null pointer. Otherwise, it returns **this** to signal success.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_filebuf Class](../vs140/basic_filebuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)