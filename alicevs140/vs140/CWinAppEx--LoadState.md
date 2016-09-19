---
title: "CWinAppEx::LoadState"
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
ms.assetid: ef5b6643-dd5b-4d2c-9ad5-b56261661c6e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::LoadState
Reads the application state from the Windows registry.  
  
## Syntax  
  
```  
BOOL LoadState(  
   CMDIFrameWndEx* pFrame,  
   LPCTSTR lpszSectionName = NULL   
);  
BOOL LoadState(  
   CFrameWndEx* pFrame,  
   LPCTSTR lpszSectionName = NULL   
);  
BOOL LoadState(  
   COleIPFrameWndEx* pFrame,  
   LPCTSTR lpszSectionName = NULL   
);  
virtual BOOL LoadState(  
   LPCTSTR lpszSectionName = NULL,  
   CFrameImpl* pFrameImpl = NULL   
);  
```  
  
#### Parameters  
 [in] `pFrame`  
 A pointer to a frame window object. The method applies the state information in the registry to this frame window.  
  
 [in] `lpszSectionName`  
 A string that contains the relative path of a registry key.  
  
 [in] `pFrameImpl`  
 A pointer to a `CFrameImpl` object. The method applies the state information in the registry to this frame window.  
  
## Return Value  
 Nonzero if successful; 0 otherwise.  
  
## Remarks  
 This method loads the state of the application and any state information for a frame window. The loaded information for the frame window is applied to the supplied frame window. If you do not supply a frame window, only the application state information is loaded. The application information includes the state of the [CMouseManager Class](../vs140/CMouseManager-Class.md), [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md), [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md), and the [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md).  
  
 The default implementation of `CFrameImpl::OnLoadFrame` calls `LoadState`.  
  
 The `lpszSectionName` parameter is not the absolute path for a registry entry. It is a relative path that is added to the end of the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md) respectively.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::SaveState](../vs140/CWinAppEx--SaveState.md)