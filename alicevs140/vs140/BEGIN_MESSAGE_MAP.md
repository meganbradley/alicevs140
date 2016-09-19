---
title: "BEGIN_MESSAGE_MAP"
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
ms.assetid: d9201e18-04e0-4639-9810-f15768627fc2
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_MESSAGE_MAP
Begins the definition of your message map.  
  
## Syntax  
  
```  
  
BEGIN_MESSAGE_MAP(  
theClass  
,   
baseClass )  
```  
  
#### Parameters  
 `theClass`  
 Specifies the name of the class whose message map this is.  
  
 `baseClass`  
 Specifies the name of the base class of `theClass`.  
  
## Remarks  
 In the implementation (.cpp) file that defines the member functions for your class, start the message map with the `BEGIN_MESSAGE_MAP` macro, then add macro entries for each of your message-handler functions, and complete the message map with the `END_MESSAGE_MAP` macro.  
  
 For more information about message maps, see [Message Maps (MFC)](../vs140/Message-Maps--MFC-.md)  
  
## Example  
 [!CODE [NVC_MFCListView#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCListView#10)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Message Maps (MFC)](../vs140/Message-Maps--MFC-.md)   
 [DECLARE_MESSAGE_MAP](../vs140/DECLARE_MESSAGE_MAP.md)   
 [END_MESSAGE_MAP](../vs140/END_MESSAGE_MAP.md)   
 [BEGIN_TEMPLATE_MESSAGE_MAP](../vs140/BEGIN_TEMPLATE_MESSAGE_MAP.md)