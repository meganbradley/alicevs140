---
title: "COleClientItem::CopyToClipboard"
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
ms.assetid: f5211e32-d17e-4269-a98f-8f82cfc0ad49
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::CopyToClipboard
Call this function to copy the OLE item to the Clipboard.  
  
## Syntax  
  
```  
  
      void CopyToClipboard(  
   BOOL bIncludeLink = FALSE   
);  
```  
  
#### Parameters  
 `bIncludeLink`  
 **TRUE** if link information should be copied to the Clipboard, allowing a linked item to be pasted; otherwise **FALSE**.  
  
## Remarks  
 Typically, you call this function when writing message handlers for the Copy or Cut commands from the Edit menu. You must implement item selection in your container application if you want to implement the Copy or Cut commands.  
  
 For more information, see [OleSetClipboard](http://msdn.microsoft.com/library/windows/desktop/ms686623) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)