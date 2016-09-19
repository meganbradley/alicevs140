---
title: "basic_ostream::sentry"
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
ms.assetid: 60925fdb-c030-40cb-8c24-3c9df81eaed5
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ostream::sentry
The nested class describes an object whose declaration structures the formatted output functions and the unformatted output functions.  
  
## Syntax  
  
```  
class sentry {  
public:  
    explicit sentry( basic_ostream<_Elem, _Tr>& _Ostr );  
    operator bool( ) const;  
    ~sentry( );  
};  
```  
  
## Remarks  
 The nested class describes an object whose declaration structures the formatted output functions and the unformatted output functions. If **ostr.**[good](../vs140/basic_ios--good.md) is **true** and **ostr.**[tie](../vs140/basic_ios--tie.md) is not a null pointer, the constructor calls **ostr.tie->**[flush](../vs140/basic_ostream--flush.md). The constructor then stores the value returned by **ostr.good** in **status**. A later call to **operator bool** delivers this stored value.  
  
 If `uncaught_exception` returns **false** and [flags](../vs140/ios_base--flags.md) **&** [unitbuf](../vs140/unitbuf.md) is nonzero, the destructor calls [flush](../vs140/basic_ostream--flush.md).  
  
## Requirements  
 **Header:** <ostream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ostream Class](../vs140/basic_ostream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)