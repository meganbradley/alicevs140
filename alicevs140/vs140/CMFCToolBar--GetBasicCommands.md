---
title: "CMFCToolBar::GetBasicCommands"
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
ms.assetid: 87577340-f396-42d0-bee0-2306bbe6f6e7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetBasicCommands
Returns a read-only list of the basic commands defined in the application.  
  
## Syntax  
  
```  
static const CList<UINT,UINT>& GetBasicCommands();  
```  
  
## Return Value  
 A const reference to a [CList](../vs140/CList-Class.md) object that contains a collection of basic commands.  
  
## Remarks  
 Add basic commands by calling [CMFCToolBar::AddBasicCommand](../vs140/CMFCToolBar--AddBasicCommand.md) or [CMFCToolBar::SetBasicCommands](../vs140/CMFCToolBar--SetBasicCommands.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)