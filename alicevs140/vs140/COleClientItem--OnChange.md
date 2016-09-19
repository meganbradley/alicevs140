---
title: "COleClientItem::OnChange"
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
ms.assetid: 27e57113-1d31-4ab9-bffd-ca3ceea6c3d2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnChange
Called by the framework when the user modifies, saves, or closes the OLE item.  
  
## Syntax  
  
```  
  
      virtual void OnChange(  
   OLE_NOTIFICATION nCode,  
   DWORD dwParam   
);  
```  
  
#### Parameters  
 `nCode`  
 The reason the server changed this item. It can have one of the following values:  
  
-   `OLE_CHANGED` The OLE item's appearance has changed.  
  
-   `OLE_SAVED` The OLE item has been saved.  
  
-   `OLE_CLOSED` The OLE item has been closed.  
  
-   `OLE_CHANGED_STATE` The OLE item has changed from one state to another.  
  
 `dwParam`  
 If `nCode` is `OLE_SAVED` or `OLE_CLOSED`, this parameter is not used. If `nCode` is `OLE_CHANGED`, this parameter specifies the aspect of the OLE item that has changed. For possible values, see the `dwParam` parameter of [COleClientItem::Draw](../vs140/COleClientItem--Draw.md). If `nCode` is `OLE_CHANGED_STATE`, this parameter is a **COleClientItem::ItemState** enumerated value and describes the state being entered. It can have one of the following values: `emptyState`, **loadedState**, `openState`, `activeState`, or `activeUIState`.  
  
## Remarks  
 (If the server application is written using the Microsoft Foundation Class Library, this function is called in response to the `Notify` member functions of `COleServerDoc` or `COleServerItem`.) The default implementation marks the container document as modified if `nCode` is `OLE_CHANGED` or `OLE_SAVED`.  
  
 For `OLE_CHANGED_STATE`, the current state returned from [GetItemState](../vs140/COleClientItem--GetItemState.md) will still be the old state, meaning the state that was current prior to this state change.  
  
 Override this function to respond to changes in the OLE item's state. Typically you update the item's appearance by invalidating the area in which the item is displayed. Call the base class implementation at the beginning of your override.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::GetItemState](../vs140/COleClientItem--GetItemState.md)   
 [COleServerItem::NotifyChanged](../vs140/COleServerItem--NotifyChanged.md)   
 [COleServerDoc::NotifyChanged](../vs140/COleServerDoc--NotifyChanged.md)   
 [COleServerDoc::NotifyClosed](../vs140/COleServerDoc--NotifyClosed.md)   
 [COleServerDoc::NotifySaved](../vs140/COleServerDoc--NotifySaved.md)