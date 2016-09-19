---
title: "basic_ifstream::open"
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
ms.assetid: 51ec9a87-ab28-44a1-9854-963d29373634
caps.latest.revision: 21
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_ifstream::open
Opens a file.  
  
## Syntax  
  
```  
void open(  
    const char *_Filename,  
    ios_base::openmode _Mode = ios_base::in,  
    int _Prot = (int)ios_base::_Openprot  
);  
void open(  
    const char *_Filename,  
    ios_base::openmode _Mode  
);  
void open(  
    const wchar_t *_Filename,  
    ios_base::openmode _Mode = ios_base::in,  
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
 The member function calls [rdbuf](../vs140/basic_ifstream--rdbuf.md) **->** [open](../vs140/basic_filebuf--open.md)(_*Filename*, `_Mode` &#124; **ios_base::in**). If open fails, the function calls [setstate](../vs140/basic_ios--setstate.md)(**failbit**), which may throw an ios_base::failure exception.  
  
## Example  
 See [basic_filebuf::open](../vs140/basic_filebuf--open.md) for an example that uses **open**.  
  
## Requirements  
 **Header:** <fstream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ifstream Class](../vs140/basic_ifstream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)