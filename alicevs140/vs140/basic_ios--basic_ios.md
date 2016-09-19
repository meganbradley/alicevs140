---
title: "basic_ios::basic_ios"
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
ms.assetid: b40911ae-93cb-42f0-8794-c801228cc8a3
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_ios::basic_ios
Constructs the basic_ios class.  
  
## Syntax  
  
```  
  
      explicit basic  
      _  
      ios(  
   basic_streambuf<_Elem,  
   _Traits> *_Sb  
);  
basic_ios();  
```  
  
#### Parameters  
 `_Sb`  
 Standard buffer to store input or output elements.  
  
## Remarks  
 The first constructor initializes its member objects by calling [init](../vs140/basic_ios--init.md)(_*Sb*). The second (protected) constructor leaves its member objects uninitialized. A later call to **init** must initialize the object before it can be safely destroyed.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)