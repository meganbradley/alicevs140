---
title: "CWinAppEx::GetShellManager"
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
ms.assetid: 4982591b-2426-47d4-acfc-6f9607b67d67
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetShellManager
Returns a pointer to the global [CShellManager](../vs140/CShellManager-Class.md) object.  
  
## Syntax  
  
```  
CShellManager* GetShellManager();  
```  
  
## Return Value  
 A pointer to the global `CShellManager` object.  
  
## Remarks  
 If the `CShellManager` object is not initialized, this function calls [CWinAppEx::InitShellManager](../vs140/CWinAppEx--InitShellManager.md) before it returns a pointer.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::InitShellManager](../vs140/CWinAppEx--InitShellManager.md)   
 [CShellManager Class](../vs140/CShellManager-Class.md)