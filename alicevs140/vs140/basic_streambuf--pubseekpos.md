---
title: "basic_streambuf::pubseekpos"
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
ms.assetid: 688015ee-cdad-4325-8366-f7ca7842f5f2
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::pubseekpos
Calls [seekpos](../vs140/basic_streambuf--seekpos.md), a protected virtual function that is overridden in a derived class, and resets the current pointer position.  
  
## Syntax  
  
```  
  
      pos  
      _  
      type pubseekpos(  
   pos_type _Sp,  
   ios_base::openmode _Which = ios_base::in | ios_base::out  
);  
```  
  
#### Parameters  
 `_Sp`  
 The position to seek for.  
  
 `_Which`  
 Specifies the mode for the pointer position. The default is to allow you to modify the read and write positions.  
  
## Return Value  
 The new position or an invalid stream position. To determine if the stream position is invalid, compare the return value with `pos_type(off_type(-1))`.  
  
## Remarks  
 The member function returns [seekpos](../vs140/basic_streambuf--seekpos.md)(_*Sp*, `_Which`).  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)