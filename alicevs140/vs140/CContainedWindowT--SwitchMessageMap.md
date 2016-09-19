---
title: "CContainedWindowT::SwitchMessageMap"
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
ms.assetid: 03ce5d5a-f47b-43d5-883f-b38c83d639ca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContainedWindowT::SwitchMessageMap
Changes which message map will be used to process the contained window's messages.  
  
## Syntax  
  
```  
  
      void SwitchMessageMap(  
   DWORD dwMsgMapID   
);  
```  
  
#### Parameters  
 `dwMsgMapID`  
 [in] The message map identifier. To use the default message map declared with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md), pass zero. To use an alternate message map declared with [ALT_MSG_MAP(msgMapID)](../vs140/ALT_MSG_MAP.md), pass `msgMapID`.  
  
## Remarks  
 The message map must be defined in the containing object.  
  
 You initially specify the message map identifier in the constructor.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CContainedWindowT Class](../vs140/CContainedWindowT-Class.md)   
 [CContainedWindowT::CContainedWindowT](../vs140/CContainedWindowT--CContainedWindowT.md)   
 [CContainedWindowT::m_dwMsgMapID](../vs140/CContainedWindowT--m_dwMsgMapID.md)