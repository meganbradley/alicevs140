---
title: "CWinAppEx::SaveCustomState"
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
ms.assetid: 80ee8b5a-a69d-478d-a340-2a95e4616be1
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::SaveCustomState
The framework calls this method after it saves the state of the application to the registry.  
  
## Syntax  
  
```  
virtual void SaveCustomState();  
```  
  
## Remarks  
 Override this method if you want to do any processing after the application saves the state to the registry. By default, this method does nothing.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::LoadCustomState](../vs140/CWinAppEx--LoadCustomState.md)