---
title: "basic_ifstream::is_open"
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
ms.assetid: 5dc6568b-5c8c-49e0-af39-bee11deae4fc
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_ifstream::is_open
Determines if a file is open.  
  
## Syntax  
  
```  
bool is_open( ) const;  
```  
  
## Return Value  
 **true** if the file is open, **false** otherwise.  
  
## Remarks  
 The member function returns [rdbuf](../vs140/basic_ifstream--rdbuf.md) **->** [is_open](../vs140/basic_filebuf--is_open.md).  
  
## Example  
 See [basic_filebuf::is_open](../vs140/basic_filebuf--is_open.md) for an example that uses `is_open`.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ifstream Class](../vs140/basic_ifstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)