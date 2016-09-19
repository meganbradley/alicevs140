---
title: "COleDataSource::FlushClipboard"
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
ms.assetid: 9636a5b8-2f99-4dc8-990d-57962da01c04
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDataSource::FlushClipboard
Renders data that is on the Clipboard, and then lets you paste data from the Clipboard after your application shuts down.  
  
## Syntax  
  
```  
static void PASCAL FlushClipboard( );  
```  
  
## Remarks  
 Use [SetClipboard](../vs140/COleDataSource--SetClipboard.md) to put data on the Clipboard.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::GetClipboardOwner](../vs140/COleDataSource--GetClipboardOwner.md)   
 [COleDataSource::SetClipboard](../vs140/COleDataSource--SetClipboard.md)