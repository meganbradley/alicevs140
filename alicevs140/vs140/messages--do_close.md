---
title: "messages::do_close"
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
ms.assetid: 04523e0c-8721-4d77-a7e7-12ffdb5d0fb9
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# messages::do_close
A virtual function called to lose the message catalog.  
  
## Syntax  
  
```  
virtual void do_close(  
    catalog _Catval  
) const;  
```  
  
#### Parameters  
 `_Catval`  
 The catalog to be closed.  
  
## Remarks  
 The protected member function closes the message catalog `_Catval`, which must have been opened by an earlier call to [do_open](../vs140/messages--do_open.md).  
  
 *_Catval* must be obtained from a previously opened catalog that is not closed.  
  
## Example  
 See the example for [close](../vs140/messages--close.md), which calls `do_close`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [messages Class](../vs140/messages-Class.md)