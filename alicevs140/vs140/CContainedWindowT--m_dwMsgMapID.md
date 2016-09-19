---
title: "CContainedWindowT::m_dwMsgMapID"
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
ms.topic: reference
ms.assetid: 0a513438-4858-4449-ab45-522341008988
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContainedWindowT::m_dwMsgMapID
Holds the identifier of the message map currently being used for the contained window.  
  
## Syntax  
  
```  
  
DWORD m_dwMsgMapID;  
  
```  
  
## Remarks  
 This message map must be declared in the containing object.  
  
 The default message map, declared with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md), is always identified by zero. An alternate message map, declared with [ALT_MSG_MAP(msgMapID)](../vs140/ALT_MSG_MAP.md), is identified by `msgMapID`.  
  
 `m_dwMsgMapID` is first initialized by the constructor and can be changed by calling [SwitchMessageMap](../vs140/CContainedWindowT--SwitchMessageMap.md). For an example, see the [CContainedWindowT Overview](../vs140/CContainedWindowT-Class.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CContainedWindowT Class](../vs140/CContainedWindowT-Class.md)   
 [CContainedWindowT::m_pObject](../vs140/CContainedWindowT--m_pObject.md)