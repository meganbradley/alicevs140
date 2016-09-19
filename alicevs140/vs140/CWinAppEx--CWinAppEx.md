---
title: "CWinAppEx::CWinAppEx"
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
ms.assetid: 1d47a941-c900-41b8-8527-ecd97f04c2f2
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::CWinAppEx
Constructs a `CWinAppEx` object.  
  
## Syntax  
  
```  
CWinAppEx(  
   BOOL bResourceSmartUpdate = FALSE  
);  
```  
  
#### Parameters  
 [in] `bResourceSmartUpdate`  
 A Boolean parameter that specifies whether the workspace object should detect and handle resource updates.  
  
## Remarks  
 The `CWinAppEx` class has initialization methods, provides functionality for saving and loading application information to the registry, and controls global application settings. It also enables you to use global managers such as the [CKeyboardManager Class](../vs140/CKeyboardManager-Class.md) and the [CUserToolsManager Class](../vs140/CUserToolsManager-Class.md). Each application can have only one instance of the `CWinAppEx` class.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)