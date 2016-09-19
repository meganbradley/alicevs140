---
title: "CTabbedPane::m_bTabsAlwaysTop"
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
ms.assetid: 05577c9d-9ca7-44c0-a581-56cee6035b0e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabbedPane::m_bTabsAlwaysTop
The default location for tabs in the application.  
  
## Syntax  
  
```  
AFX_IMPORT_DATA static BOOL m_bTabsAlwaysTop;  
```  
  
## Remarks  
 Set this static member to `TRUE` to force all tabs in the application to be displayed at the top of the tabbed pane.  
  
 You must set this value before a tabbed pane has been created.  
  
 The default value is `FALSE`.  
  
## Requirements  
 **Header:** afxTabbedPane.h  
  
## See Also  
 [CTabbedPane Class](../vs140/CTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)