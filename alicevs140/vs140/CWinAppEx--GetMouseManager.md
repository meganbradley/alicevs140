---
title: "CWinAppEx::GetMouseManager"
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
ms.assetid: 2cb5cc4b-0e65-4704-a686-9eab10739dd6
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetMouseManager
Returns a pointer to the global [CMouseManager](../vs140/CMouseManager-Class.md) object.  
  
## Syntax  
  
```  
CMouseManager* GetMouseManager();  
```  
  
## Return Value  
 A pointer to the global `CMouseManager` object.  
  
## Remarks  
 If the mouse manager is not initialized,, this function calls [CWinAppEx::InitMouseManager](../vs140/CWinAppEx--InitMouseManager.md) before it returns a pointer.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::InitMouseManager](../vs140/CWinAppEx--InitMouseManager.md)   
 [CMouseManager Class](../vs140/CMouseManager-Class.md)