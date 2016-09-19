---
title: "COleClientItem::OnGetClipboardData"
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
ms.assetid: f5f04aa5-2fd2-4647-8242-ef3ee9232c42
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnGetClipboardData
Called by the framework to get a `COleDataSource` object containing all the data that would be placed on the Clipboard by a call to either the [CopyToClipboard](../vs140/COleClientItem--CopyToClipboard.md) or the [DoDragDrop](../vs140/COleClientItem--DoDragDrop.md) member function.  
  
## Syntax  
  
```  
  
      virtual COleDataSource* OnGetClipboardData(  
   BOOL bIncludeLink,  
   LPPOINT lpOffset,  
   LPSIZE lpSize   
);  
```  
  
#### Parameters  
 `bIncludeLink`  
 Set this to **TRUE** if link data should be copied to the Clipboard. Set this to **FALSE** if your server application does not support links.  
  
 `lpOffset`  
 Pointer to the offset of the mouse cursor from the origin of the object in pixels.  
  
 `lpSize`  
 Pointer to the size of the object in pixels.  
  
## Return Value  
 A pointer to a [COleDataSource](../Topic/COleDataSource%20Class.md) object containing the Clipboard data.  
  
## Remarks  
 The default implementation of this function calls [GetClipboardData](../vs140/COleClientItem--GetClipboardData.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [COleClientItem::CopyToClipboard](../vs140/COleClientItem--CopyToClipboard.md)   
 [COleClientItem::GetClipboardData](../vs140/COleClientItem--GetClipboardData.md)   
 [COleDataSource::SetClipboard](../vs140/COleDataSource--SetClipboard.md)