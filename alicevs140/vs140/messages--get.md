---
title: "messages::get"
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
ms.assetid: f5b769b8-17a0-4622-8ba1-c6758c7faa18
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# messages::get
Retrieves the message catalog.  
  
## Syntax  
  
```  
string_type get(  
    catalog _CatVal,   
    int _Set,   
    int _Message,  
    const string_type& _Dfault  
) const;  
```  
  
#### Parameters  
 `_Catval`  
 The identification value specifying the message catalog to be searched.  
  
 `_Set`  
 The first identified used to locate a message in a message catalog.  
  
 `_Message`  
 The second identified used to locate a message in a message catalog.  
  
 `_Dfault`  
 The string to be returned on failure.  
  
## Return Value  
 It returns a copy of `_Dfault` on failure. Otherwise, it returns a copy of the specified message sequence.  
  
## Remarks  
 The member function returns [do_get](../vs140/messages--do_get.md)(`_Catval`, `_Set`, `_Message`, `_Dfault`).  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [messages Class](../vs140/messages-Class.md)