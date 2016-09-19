---
title: "COleServerItem::CopyToClipboard"
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
ms.assetid: ed7b33a0-ab33-43e1-9881-5a75f039d7fe
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::CopyToClipboard
Call this function to copy the OLE item to the Clipboard.  
  
## Syntax  
  
```  
  
      void CopyToClipboard(  
   BOOL bIncludeLink = FALSE   
);   
```  
  
#### Parameters  
 `bIncludeLink`  
 Set this to **TRUE** if link data should be copied to the Clipboard. Set this to **FALSE** if your server application does not support links.  
  
## Remarks  
 The function uses the [OnGetClipboardData](../vs140/COleServerItem--OnGetClipboardData.md) member function to create a [COleDataSource](../Topic/COleDataSource%20Class.md) object containing the OLE item's data in the formats supported. The function then places the `COleDataSource` object on the Clipboard by using the [COleDataSource::SetClipboard](../vs140/COleDataSource--SetClipboard.md) function. The `COleDataSource` object includes the item's native data and its representation in `CF_METAFILEPICT` format, as well as data in any conversion formats you choose to support. You must have implemented [Serialize](../vs140/CObject--Serialize.md) and [OnDraw](../vs140/COleServerItem--OnDraw.md) for this member function to work.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataSource::SetClipboard](../vs140/COleDataSource--SetClipboard.md)   
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [COleServerItem::AddOtherClipboardData](../vs140/COleServerItem--AddOtherClipboardData.md)   
 [COleServerItem::GetClipboardData](../vs140/COleServerItem--GetClipboardData.md)   
 [COleServerItem::OnDraw](../vs140/COleServerItem--OnDraw.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)