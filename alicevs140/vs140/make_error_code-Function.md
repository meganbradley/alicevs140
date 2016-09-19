---
title: "make_error_code Function"
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
ms.assetid: 67099884-698e-40e5-ae4a-1e3f13e9e7b0
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# make_error_code Function
Creates an [error_code](../vs140/error_code-Class.md) together with the [error_category](../vs140/error_category-Class.md) object that characterizes [future](../vs140/future-Class.md) errors.  
  
## Syntax  
  
```  
inline error_code make_error_code(  
   future_errc Errno  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Errno`  
 A [future_errc](../vs140/future_errc-Enumeration.md) value that identifies the reported error.  
  
## Return Value  
 `error_code(static_cast<int>(Errno), future_category());`  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<future\>](../vs140/-future-.md)