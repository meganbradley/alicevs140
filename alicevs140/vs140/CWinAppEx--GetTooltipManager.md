---
title: "CWinAppEx::GetTooltipManager"
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
ms.assetid: 7e56ae86-cb18-4f0f-83f4-1d5c53d0cd26
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::GetTooltipManager
Returns a pointer to the global [CTooltipManager](../vs140/CTooltipManager-Class.md) object.  
  
## Syntax  
  
```  
CTooltipManager* GetTooltipManager();  
```  
  
## Return Value  
 A pointer to the global `CTooltipManager` object.  
  
## Remarks  
 If the `CTooltipManager` object is not initialized, this function calls [CWinAppEx::InitTooltipManager](../vs140/CWinAppEx--InitTooltipManager.md) before it returns a pointer.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::InitTooltipManager](../vs140/CWinAppEx--InitTooltipManager.md)   
 [CTooltipManager Class](../vs140/CTooltipManager-Class.md)