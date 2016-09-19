---
title: "CWinAppEx::PreSaveState"
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
ms.assetid: 61c5c221-0088-497a-8540-a5d4ff942a40
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::PreSaveState
The framework calls this method immediately before it saves the application state.  
  
## Syntax  
  
```  
virtual void PreSaveState();  
```  
  
## Remarks  
 Override this method if you want to do any processing immediately before the framework saves the application state.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)