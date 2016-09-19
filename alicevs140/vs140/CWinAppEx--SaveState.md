---
title: "CWinAppEx::SaveState"
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
ms.assetid: 9ea6b353-7c00-4a76-86c5-d5e3ce6f6b56
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::SaveState
Writes the application state to the Windows registry.  
  
## Syntax  
  
```  
virtual BOOL SaveState(  
   LPCTSTR lpszSectionName = NULL,  
   CFrameImpl* pFrameImpl = NULL   
);  
BOOL SaveState(  
   CMDIFrameWndEx* pFrame,  
   LPCTSTR lpszSectionName = NULL   
);  
BOOL SaveState(  
   CFrameWndEx* pFrame,  
   LPCTSTR lpszSectionName = NULL   
);  
BOOL SaveState(  
   COleIPFrameWndEx* pFrame,  
   LPCTSTR lpszSectionName = NULL   
);  
```  
  
#### Parameters  
 [in] `lpszSectionName`  
 A string that contains the relative path of a registry key.  
  
 [in] `pFrameImpl`  
 A pointer to a `CFrameImpl` object. This frame is saved to the Windows registry.  
  
 [in] `pFrame`  
 A pointer to a frame window object. This frame is saved to the Windows registry.  
  
## Return Value  
 `True` if successful; `false` otherwise.  
  
## Remarks  
 This method saves the state of the application and any state information for the provided frame window. If you do not provide a frame window, the method only saves the application state. The application information includes the state of the [CMouseManager Class](../vs140/CMouseManager-Class.md), [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md), [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md), and the [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md).  
  
 The `lpszSectionName` parameter is not the absolute path for a registry entry. It is a relative path that is appended to the end of the default registry key for your application. To get or set the default registry key, use the methods [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md) and [CWinAppEx::SetRegistryBase](../vs140/CWinAppEx--SetRegistryBase.md) respectively.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::LoadState](../vs140/CWinAppEx--LoadState.md)