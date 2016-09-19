---
title: "basic_fstream::open"
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
ms.assetid: 464af71a-0a9b-4ae7-aa9e-4db57b7e1a04
caps.latest.revision: 21
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_fstream::open
Opens a file.  
  
## Syntax  
  
```  
void open(  
    const char *_Filename,  
    ios_base::openmode _Mode = ios_base::in | ios_base::out,  
    int _Prot = (int)ios_base::_Openprot  
);  
void open(  
    const char *_Filename,  
    ios_base::openmode _Mode  
);  
void open(  
    const wchar_t *_Filename,  
    ios_base::openmode _Mode = ios_base::in | ios_base::out,  
    int _Prot = (int)ios_base::_Openprot  
);  
void open(  
    const wchar_t *_Filename,  
    ios_base::openmode _Mode  
);  
```  
  
#### Parameters  
 `_Filename`  
 The name of the file to open.  
  
 `_Mode`  
 One of the enumerations in [ios_base::openmode](../vs140/ios_base--openmode.md).  
  
 `_Prot`  
 The default file opening protection, equivalent to the `shflag` parameter in [_fsopen, _wsfopen](../Topic/_fsopen,%20_wfsopen.md).  
  
## Remarks  
 The member function calls [rdbuf](../vs140/basic_fstream--rdbuf.md) **->** [open](../vs140/basic_filebuf--open.md)(_*Filename*, `_Mode`). If that function returns a null pointer, the function calls [setstate](../vs140/basic_ios--setstate.md)(**failbit**).  
  
## Example  
 See [basic_filebuf::open](../vs140/basic_filebuf--open.md) for an example of how to use **open**.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_fstream Class](../vs140/basic_fstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)