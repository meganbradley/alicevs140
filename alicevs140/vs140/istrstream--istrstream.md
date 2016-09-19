---
title: "istrstream::istrstream"
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
ms.assetid: fccaf0fa-7769-47f9-9884-7a286a61a130
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# istrstream::istrstream
Constructs an object of type `istrstream`.  
  
## Syntax  
  
```  
explicit istrstream(  
    const char *_Ptr  
);  
explicit istrstream(  
    char *_Ptr  
);  
istrstream(  
    const char *_Ptr,   
    streamsize _Count  
);  
istrstream(  
    char *_Ptr,   
    int _Count  
);  
```  
  
#### Parameters  
 `_Count`  
 The length of the buffer (`_Ptr`).  
  
 `_Ptr`  
 The contents with which the buffer is initialized.  
  
## Remarks  
 All the constructors initialize the base class by calling [istream](../vs140/istream.md)(**sb**), where **sb** is the stored object of class [strstreambuf](../vs140/strstreambuf-Class.md). The first two constructors also initialize **sb** by calling `strstreambuf`( (**const** `char` \*)`_Ptr`, 0 ). The remaining two constructors instead call `strstreambuf`( (**const** `char` *)`_Ptr`, `_Count` ).  
  
## Requirements  
 **Header:** <strstream\>  
  
 **Namespace:** std  
  
## See Also  
 [istrstream Class](../vs140/istrstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)