---
title: "COleServerItem::OnGetClipboardData"
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
ms.assetid: bd26d0ed-c9a8-4dc8-b996-67fde63f5ed1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnGetClipboardData
Called by the framework to get a `COleDataSource` object containing all the data that would be placed on the Clipboard by a call to the [CopyToClipboard](../vs140/COleServerItem--CopyToClipboard.md) member function.  
  
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
 The offset of the mouse cursor from the origin of the object in pixels.  
  
 `lpSize`  
 The size of the object in pixels.  
  
## Return Value  
 A pointer to a [COleDataSource](../Topic/COleDataSource%20Class.md) object containing the Clipboard data.  
  
## Remarks  
 The default implementation of this function calls [GetClipboardData](../vs140/COleServerItem--GetClipboardData.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [COleDataSource::SetClipboard](../vs140/COleDataSource--SetClipboard.md)   
 [COleServerItem::CopyToClipboard](../vs140/COleServerItem--CopyToClipboard.md)   
 [COleServerItem::GetClipboardData](../vs140/COleServerItem--GetClipboardData.md)