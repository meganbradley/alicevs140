---
title: "make_error_condition Function"
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
ms.assetid: 552f01e5-87fd-410f-a3c9-31bf194a8b38
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# make_error_condition Function
Creates an [error_condition](../vs140/error_condition-Class.md) together with the [error_category](../vs140/error_category-Class.md) object that characterizes [future](../vs140/future-Class.md) errors.  
  
## Syntax  
  
```  
inline error_condition make_error_condition(  
   future_errc Errno  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Errno`  
 A [future_errc](../vs140/future_errc-Enumeration.md) value that identifies the reported error.  
  
## Return Value  
 `error_condition(static_cast<int>(Errno), future_category());`  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<future\>](../vs140/-future-.md)