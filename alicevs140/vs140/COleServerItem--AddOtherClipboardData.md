---
title: "COleServerItem::AddOtherClipboardData"
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
ms.assetid: dbfd884f-bea3-4179-b7eb-c47678bf1c63
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::AddOtherClipboardData
Call this function to place the presentation and conversion formats for the OLE item in the specified `COleDataSource` object.  
  
## Syntax  
  
```  
  
      void AddOtherClipboardData(  
   COleDataSource* pDataSource   
);  
```  
  
#### Parameters  
 `pDataSource`  
 Pointer to the `COleDataSource` object in which the data should be placed.  
  
## Remarks  
 You must have implemented the [OnDraw](../vs140/COleServerItem--OnDraw.md) member function to provide the presentation format (a metafile picture) for the item. To support other conversion formats, register them using the [COleDataSource](../Topic/COleDataSource%20Class.md) object returned by [GetDataSource](../vs140/COleServerItem--GetDataSource.md) and override the [OnRenderData](../vs140/COleServerItem--OnRenderData.md) member function to provide data in the formats you want to support.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [COleServerItem::GetDataSource](../vs140/COleServerItem--GetDataSource.md)   
 [COleServerItem::GetEmbedSourceData](../vs140/COleServerItem--GetEmbedSourceData.md)   
 [COleServerItem::OnDraw](../vs140/COleServerItem--OnDraw.md)