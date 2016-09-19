---
title: "messages::do_open"
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
ms.assetid: 859ae6c9-23e2-4c83-ad50-721baf3374c3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# messages::do_open
A virtual function called to open the message catalog.  
  
## Syntax  
  
```  
virtual catalog do_open(  
    const string& _Catname,  
    const locale& _Loc  
) const;  
```  
  
#### Parameters  
 `_Catname`  
 The name of the catalog to be searched.  
  
 `_Loc`  
 The locale being searched for in the catalog.  
  
## Return Value  
 It returns a value that compares less than zero on failure. Otherwise, the returned value can be used as the first argument on a later call to [get](../vs140/messages--get.md).  
  
## Remarks  
 The protected member function tries to open a message catalog whose name is `_Catname`. It may make use of the locale `_Loc` in doing so  
  
 The return value should be used as the argument on a later call to [close](../vs140/messages--close.md).  
  
## Example  
 See the example for [open](../vs140/messages--open.md), which calls `do_open`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [messages Class](../vs140/messages-Class.md)