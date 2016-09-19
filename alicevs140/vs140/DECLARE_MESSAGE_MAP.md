---
title: "DECLARE_MESSAGE_MAP"
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
ms.assetid: c225e7e0-a81b-495c-97f9-3e0aa1f65036
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_MESSAGE_MAP
Declares that the class defines a message map. Each `CCmdTarget`-derived class in your program must provide a message map to handle messages.  
  
## Syntax  
  
```  
  
DECLARE_MESSAGE_MAP( )  
```  
  
## Remarks  
 Use the `DECLARE_MESSAGE_MAP` macro at the end of your class declaration. Then, in the .cpp file that defines the member functions for the class, use the `BEGIN_MESSAGE_MAP` macro, macro entries for each of your message-handler functions, and the `END_MESSAGE_MAP` macro.  
  
> [!NOTE]
>  If you declare any member after `DECLARE_MESSAGE_MAP`, you must specify a new access type (**public**, `private`, or `protected`) for them.  
  
 For more information on message maps and the `DECLARE_MESSAGE_MAP` macro, see [Message Handling and Mapping Topics](../vs140/Message-Handling-and-Mapping.md).  
  
## Example  
 [!CODE [NVC_MFCWindowing#136](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#136)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_MESSAGE_MAP](../vs140/BEGIN_MESSAGE_MAP.md)   
 [END_MESSAGE_MAP](../vs140/END_MESSAGE_MAP.md)