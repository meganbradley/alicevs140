---
title: "basic_ostream::tellp"
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
ms.assetid: 3e10107e-7ec2-4b98-b271-bfb69cb52a76
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ostream::tellp
Report position in output stream.  
  
## Syntax  
  
```  
pos_type tellp( );  
```  
  
## Return Value  
 Position in output stream.  
  
## Remarks  
 If [fail](../vs140/basic_ios--fail.md) is **false**, the member function returns [rdbuf](../vs140/basic_ios--rdbuf.md)**->** [pubseekoff](../vs140/basic_streambuf--pubseekoff.md)(0, `cur`, **in**). Otherwise, it returns `pos_type`(-1).  
  
## Example  
 See [seekp](../vs140/basic_ostream--seekp.md) for an example using `tellp`.  
  
## Requirements  
 **Header:** <ostream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ostream Class](../vs140/basic_ostream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)