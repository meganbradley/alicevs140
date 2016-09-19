---
title: "CDynamicChain::CallChain"
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
ms.assetid: d958dfcd-9e01-497e-a387-4290e5da2f9c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDynamicChain::CallChain
Directs the Windows message to another object's message map.  
  
## Syntax  
  
```  
  
      BOOL CallChain(  
   DWORD dwChainID,  
   HWND hWnd,  
   UINT uMsg,  
   WPARAM wParam,  
   LPARAM lParam,  
   LRESULT& lResult   
);  
```  
  
#### Parameters  
 `dwChainID`  
 [in] The unique identifier associated with the chained object and its message map.  
  
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
  
## Return Value  
 **TRUE** if the message is fully processed; otherwise, **FALSE**.  
  
## Remarks  
 For the window procedure to invoke `CallChain`, you must specify the [CHAIN_MSG_MAP_DYNAMIC](../vs140/CHAIN_MSG_MAP_DYNAMIC.md) macro in your message map. For an example, see the [CDynamicChain](../vs140/CDynamicChain-Class.md) overview.  
  
 `CallChain` requires a previous call to [SetChainEntry](../vs140/CDynamicChain--SetChainEntry.md) to associate the `dwChainID` value with an object and its message map.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CDynamicChain Class](../vs140/CDynamicChain-Class.md)