---
title: "COleDataSource::GetClipboardOwner"
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
ms.assetid: d68d53fb-bbf4-4c93-8043-9748033725e6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataSource::GetClipboardOwner
Determines whether the data on the Clipboard has changed since [SetClipboard](../vs140/COleDataSource--SetClipboard.md) was last called and, if so, identifies the current owner.  
  
## Syntax  
  
```  
  
static COleDataSource* PASCAL GetClipboardOwner( );  
```  
  
## Return Value  
 The data source currently on the Clipboard, or **NULL** if there is nothing on the Clipboard or if the Clipboard is not owned by the calling application.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::FlushClipboard](../vs140/COleDataSource--FlushClipboard.md)   
 [COleDataSource::SetClipboard](../vs140/COleDataSource--SetClipboard.md)