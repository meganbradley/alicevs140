---
title: "CKeyboardManager::FindDefaultAccelerator"
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
ms.assetid: ee88c556-b174-4794-bbf3-101d29aed707
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyboardManager::FindDefaultAccelerator
Retrieves the default shortcut key for the specified command and window.  
  
## Syntax  
  
```  
static BOOL FindDefaultAccelerator(  
   UINT uiCmd,  
   CString& str,  
   CFrameWnd* pWndFrame,  
   BOOL bIsDefaultFrame   
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The command ID.  
  
 [out] `str`  
 A reference to a `CString` object.  
  
 [in] `pWndFrame`  
 A pointer to a frame window.  
  
 [in] `bIsDefaultFrame`  
 Specifies whether the frame window is the default frame window.  
  
## Return Value  
 Nonzero if the shortcut is found; otherwise 0.  
  
## Remarks  
 This method looks up the command specified by `uiCmd` and retrieves the default shortcut key. Then the method takes the string associated with this shortcut key and writes the value to the `str` parameter.  
  
## Requirements  
 **Header:** afxkeyboardmanager.h  
  
## See Also  
 [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)