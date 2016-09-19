---
title: "COleClientItem::GetClipboardData"
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
ms.assetid: 8bad19ca-281a-4fe0-aa62-2bdb593c38b8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetClipboardData
Call this function to get a `COleDataSource` object containing all the data that would be placed on the Clipboard by a call to the [CopyToClipboard](../vs140/COleClientItem--CopyToClipboard.md) member function.  
  
## Syntax  
  
```  
  
      void GetClipboardData(  
   COleDataSource* pDataSource,  
   BOOL bIncludeLink = FALSE,  
   LPPOINT lpOffset = NULL,  
   LPSIZE lpSize = NULL   
);  
```  
  
#### Parameters  
 `pDataSource`  
 Pointer to a [COleDataSource](../Topic/COleDataSource%20Class.md) object that will receive the data contained in the OLE item.  
  
 `bIncludeLink`  
 **TRUE** if link data should be included; otherwise **FALSE**.  
  
 `lpOffset`  
 The offset of the mouse cursor from the origin of the object in pixels.  
  
 `lpSize`  
 The size of the object in pixels.  
  
## Remarks  
 `GetClipboardData` is called as the default implementation of [OnGetClipboardData](../vs140/COleClientItem--OnGetClipboardData.md). Override `OnGetClipboardData` only if you want to offer data formats in addition to those offered by `CopyToClipboard`. Place those formats in the `COleDataSource` object before or after calling `CopyToClipboard`, and then pass the `COleDataSource` object to the [COleDataSource::SetClipboard](../vs140/COleDataSource--SetClipboard.md) function. For example, if you want the OLE item's position in its container document to accompany it on the Clipboard, you would define your own format for passing that information and place it in the `COleDataSource` before calling `CopyToClipboard`.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [COleClientItem::CopyToClipboard](../vs140/COleClientItem--CopyToClipboard.md)   
 [COleDataSource::SetClipboard](../vs140/COleDataSource--SetClipboard.md)