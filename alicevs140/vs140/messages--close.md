---
title: "messages::close"
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
ms.assetid: f160ca8c-823c-499f-8c59-61eb3cc95d6c
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# messages::close
Closes the message catalog.  
  
## Syntax  
  
```  
void close(  
    catalog _Catval  
) const;  
```  
  
#### Parameters  
 `_Catval`  
 The catalog to be closed.  
  
## Remarks  
 The member function calls [do_close](../vs140/messages--do_close.md)(_*Catval*).  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [messages Class](../vs140/messages-Class.md)