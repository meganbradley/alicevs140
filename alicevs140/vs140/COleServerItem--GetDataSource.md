---
title: "COleServerItem::GetDataSource"
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
ms.assetid: 8bc35ff6-aece-4c01-9721-dcc62d750cdc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::GetDataSource
Call this function to get the [COleDataSource](../Topic/COleDataSource%20Class.md) object used to store the conversion formats that the server application supports.  
  
## Syntax  
  
```  
  
COleDataSource* GetDataSource( );   
```  
  
## Return Value  
 A pointer to the `COleDataSource` object used to store the conversion formats.  
  
## Remarks  
 If you want your server application to offer data in a variety of formats during data transfer operations, register those formats with the `COleDataSource` object returned by this function. For example, if you want to supply a **CF_TEXT** representation of the OLE item for Clipboard or drag-and-drop operations, you would register the format with the `COleDataSource` object this function returns, and then override the **OnRenderXxxData** member function to provide the data.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [COleDataSource::DelayRenderData](../vs140/COleDataSource--DelayRenderData.md)   
 [COleServerItem::CopyToClipboard](../vs140/COleServerItem--CopyToClipboard.md)   
 [COleServerItem::DoDragDrop](../vs140/COleServerItem--DoDragDrop.md)   
 [COleServerItem::OnRenderData](../vs140/COleServerItem--OnRenderData.md)   
 [COleServerItem::OnRenderFileData](../vs140/COleServerItem--OnRenderFileData.md)   
 [COleServerItem::OnRenderGlobalData](../vs140/COleServerItem--OnRenderGlobalData.md)