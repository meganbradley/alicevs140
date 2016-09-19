---
title: "CMDITabInfo::m_bDocumentMenu"
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
ms.assetid: 023ab05a-54c9-4cf8-9e7e-1422ab353fe8
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDITabInfo::m_bDocumentMenu
Specifies whether each tab displays a popup menu that shows a list of  opened documents at the right edge of the tab area.  
  
## Syntax  
  
```  
BOOL m_bDocumentMenu;  
```  
  
## Remarks  
 If `TRUE`, each tab windows displays a popup menu that shows a list of opened documents at the right edge of the tab area; Otherwise, the tab window displays scroll buttons at the right edge of the tab area. The default value is `FALSE`.  
  
## Requirements  
 **Header:** afxmdiclientareawnd.h  
  
## See Also  
 [CMDITabInfo Class](../vs140/CMDITabInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)