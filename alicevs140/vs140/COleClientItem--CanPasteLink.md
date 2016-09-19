---
title: "COleClientItem::CanPasteLink"
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
ms.assetid: ca61ca9c-bc06-473a-b9da-481c1e777c22
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::CanPasteLink
Call this function to see whether a linked OLE item can be pasted from the Clipboard.  
  
## Syntax  
  
```  
  
static BOOL PASCAL CanPasteLink( );  
```  
  
## Return Value  
 Nonzero if a linked OLE item can be pasted from the Clipboard; otherwise 0.  
  
## Remarks  
 For more information, see [OleGetClipboard](http://msdn.microsoft.com/library/windows/desktop/ms692778) and [OleQueryLinkFromData](http://msdn.microsoft.com/library/windows/desktop/ms690244) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::CanPaste](../vs140/COleClientItem--CanPaste.md)   
 [COleClientItem::CreateLinkFromClipboard](../vs140/COleClientItem--CreateLinkFromClipboard.md)