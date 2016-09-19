---
title: "COleClientItem::CanPaste"
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
ms.assetid: 21e649a9-4608-4c74-ad10-9f92e1d7d528
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::CanPaste
Call this function to see whether an embedded OLE item can be pasted from the Clipboard.  
  
## Syntax  
  
```  
  
static BOOL PASCAL CanPaste( );  
```  
  
## Return Value  
 Nonzero if an embedded OLE item can be pasted from the Clipboard; otherwise 0.  
  
## Remarks  
 For more information, see [OleGetClipboard](http://msdn.microsoft.com/library/windows/desktop/ms692778) and [OleQueryCreateFromData](http://msdn.microsoft.com/library/windows/desktop/ms683739) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::CanPasteLink](../vs140/COleClientItem--CanPasteLink.md)   
 [COleClientItem::CreateFromClipboard](../vs140/COleClientItem--CreateFromClipboard.md)   
 [COleClientItem::CreateStaticFromClipboard](../vs140/COleClientItem--CreateStaticFromClipboard.md)   
 [COleDocument Class](../vs140/COleDocument-Class.md)