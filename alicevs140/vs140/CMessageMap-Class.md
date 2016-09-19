---
title: "CMessageMap Class"
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
ms.assetid: 1f97bc16-a8a0-4cf0-b90f-1778813a5c8e
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMessageMap Class
This class allows an object's message maps to be access by another object.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class ATL_NO_VTABLE CMessageMap  
  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CMessageMap::ProcessWindowMessage](../vs140/CMessageMap--ProcessWindowMessage.md)|Accesses a message map in the `CMessageMap`-derived class.|  
  
## Remarks  
 `CMessageMap` is an abstract base class that allows an object's message maps to be accessed by another object. In order for an object to expose its message maps, its class must derive from `CMessageMap`.  
  
 ATL uses `CMessageMap` to support contained windows and dynamic message map chaining. For example, any class containing a [CContainedWindow](../vs140/CContainedWindowT-Class.md) object must derive from `CMessageMap`. The following code is taken from the [SUBEDIT](../vs140/Visual-C---Samples.md) sample. Through [CComControl](../vs140/CComControl-Class.md), the `CAtlEdit` class automatically derives from `CMessageMap`.  
  
 [!CODE [NVC_ATL_Windowing#90](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#90)]  
  
 Because the contained window, `m_EditCtrl`, will use a message map in the containing class, `CAtlEdit` derives from `CMessageMap`.  
  
 For more information about message maps, see [Message Maps](../vs140/Message-Maps--ATL-.md) in the article "ATL Window Classes."  
  
## Requirements  
 **Header:** atlwin.h  
  
##  <a name="cmessagemap__processwindowmessage"></a>  CMessageMap::ProcessWindowMessage  
 Accesses the message map identified by `dwMsgMapID` in a `CMessageMap`-derived class.  
  
```  
  
virtual BOOL ProcessWindowMessage(  
      HWND  hWnd,  
      UINT  uMsg,  
      WPARAM  wParam,  
      LPARAM  lParam,  
      LRESULT&  lResult,  
      DWORD  dwMsgMapID  
   ) = 0;  
  
```  
  
### Parameters  
 `hWnd`  
 [in] The handle to the window receiving the message.  
  
 `uMsg`  
 [in] The message sent to the window.  
  
 `wParam`  
 [in] Additional message-specific information.  
  
 `lParam`  
 [in] Additional message-specific information.  
  
 `lResult`  
 [out] The result of the message processing.  
  
 `dwMsgMapID`  
 [in] The identifier of the message map that will process the message. The default message map, declared with [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md), is identified by 0. An alternate message map, declared with [ALT_MSG_MAP(msgMapID)](../vs140/ALT_MSG_MAP.md), is identified by `msgMapID`.  
  
### Return Value  
 **TRUE** if the message is fully handled; otherwise,                         **FALSE**.  
  
### Remarks  
 Called by the window procedure of a [CContainedWindow](../vs140/CContainedWindowT-Class.md) object or of an object that is dynamically chaining to the message map.  
  
## See Also  
 [CDynamicChain Class](../vs140/CDynamicChain-Class.md)   
 [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md)   
 [ALT_MSG_MAP](../vs140/ALT_MSG_MAP.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)