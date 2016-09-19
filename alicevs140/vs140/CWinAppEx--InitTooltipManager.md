---
title: "CWinAppEx::InitTooltipManager"
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
ms.assetid: 69a6285e-6892-430a-93e6-bc315346bd32
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::InitTooltipManager
Initializes the [CTooltipManager](../vs140/CTooltipManager-Class.md) object.  
  
## Syntax  
  
```  
BOOL InitTooltipManager();  
```  
  
## Return Value  
 Nonzero if the method creates the `CTooltipManager` object; 0 if the `CTooltipManager` object already exists.  
  
## Remarks  
 If you call [CWinAppEx::GetTooltipManager](../vs140/CWinAppEx--GetTooltipManager.md), the default implementation of that method calls `InitTooltipManager`.  
  
 If your application already has a tooltip manager and you call `InitTooltipManager`, your application will have an [ASSERT](../vs140/ASSERT--MFC-.md) failure. Therefore, you should not call `InitTooltipManager` if you create a `CTooltipManager` object directly. If you are not using a custom `CTooltipManager`, you should use `GetTooltipManager` to create a `CTooltipManager` object.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::GetTooltipManager](../vs140/CWinAppEx--GetTooltipManager.md)   
 [CTooltipManager Class](../vs140/CTooltipManager-Class.md)