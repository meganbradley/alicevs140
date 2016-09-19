---
title: "CContainedWindowT::m_pObject"
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
ms.assetid: deb78a2c-8e32-41b3-94f8-61b382fc2b76
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContainedWindowT::m_pObject
Points to the object containing the `CContainedWindowT` object.  
  
## Syntax  
  
```  
  
CMessageMap* m_pObject;  
  
```  
  
## Remarks  
 This container, whose class must derive from [CMessageMap](../vs140/CMessageMap-Class.md), declares the message map used by the contained window.  
  
 `m_pObject` is initialized by the constructor. For an example, see the [CContainedWindowT](../vs140/CContainedWindowT-Class.md) overview.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CContainedWindowT Class](../vs140/CContainedWindowT-Class.md)   
 [CContainedWindowT::m_dwMsgMapID](../vs140/CContainedWindowT--m_dwMsgMapID.md)