---
title: "CKeyboardManager::IsKeyHandled"
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
ms.assetid: 2f7d97ce-0cc1-470d-b259-faf389550461
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CKeyboardManager::IsKeyHandled
Determines whether the specified key is handled by the [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md).  
  
## Syntax  
  
```  
static BOOL __stdcall IsKeyHandled(  
   WORD nKey,  
   BYTE fVirt,  
   CFrameWnd* pWndFrame,  
   BOOL bIsDefaultFrame  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `nKey`|The key to check.|  
|[in] `fVirt`|Specifies the behavior of the shortcut key. For a list of possible values, see [ACCEL Structure](http://msdn.microsoft.com/library/windows/desktop/ms646340).|  
|[in] `pWndFrame`|A frame window. This method determines whether a shortcut key is handled in this frame.|  
|[in] `bIsDefaultFrame`|A Boolean parameter that indicates whether `pWndFrame` is the default frame window.|  
  
## Return Value  
 `TRUE` if the shortcut key is handled. `FALSE` if the key is not handled or if `pWndFrame` is `NULL`.  
  
## Remarks  
 The input parameters must match the entry in the accelerator table both for `nKey` and `fVirt` to determine whether a shortcut key is handled in `pWndFrame`.  
  
## Requirements  
 **Header:** afxkeyboardmanager.h  
  
## See Also  
 [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)