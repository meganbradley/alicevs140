---
title: "CMDIFrameWndEx::IsMDITabbedGroup"
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
ms.assetid: 3f55632d-df7d-4a9c-9bdf-a3b4a41c5a34
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::IsMDITabbedGroup
Specifies whether the MDI Tabbed Groups feature is enabled.  
  
## Syntax  
  
```  
BOOL IsMDITabbedGroup() const;  
```  
  
## Return Value  
 `TRUE` if the MDI Tabbed Groups feature is enabled; otherwise `FALSE`.  
  
## Remarks  
 To determine whether regular MDI tabs or the MDI Tabbed Groups feature is enabled, use [CMDIFrameWndEx::AreMDITabs](../vs140/CMDIFrameWndEx--AreMDITabs.md).  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)