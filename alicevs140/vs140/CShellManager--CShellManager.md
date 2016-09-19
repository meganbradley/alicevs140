---
title: "CShellManager::CShellManager"
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
ms.assetid: d111d79a-fee9-4532-a190-790620ef6b18
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CShellManager::CShellManager
Constructs a `CShellManager` object.  
  
## Syntax  
  
```  
CShellManager();  
```  
  
## Remarks  
 In most cases, you do not have to create a `CShellManager` directly. By default, the framework creates one for you. To get a pointer to the `CShellManager`, call [CWinAppEx::GetShellManager](../vs140/CWinAppEx--GetShellManager.md). If you do create a `CShellManager` manually, you must initialize it with the method [CWinAppEx::InitShellManager](../vs140/CWinAppEx--InitShellManager.md).  
  
## Requirements  
 **Header:** afxshellmanager.h  
  
## See Also  
 [CShellManager Class](../vs140/CShellManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::GetShellManager](../vs140/CWinAppEx--GetShellManager.md)   
 [CWinAppEx::InitShellManager](../vs140/CWinAppEx--InitShellManager.md)