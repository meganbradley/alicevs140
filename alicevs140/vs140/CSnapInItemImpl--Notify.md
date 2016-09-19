---
title: "CSnapInItemImpl::Notify"
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
ms.assetid: 5bdda9a1-24b6-441c-baeb-dd0832c26261
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInItemImpl::Notify
Called when the snap-in object is acted upon by the user.  
  
## Syntax  
  
```  
  
      STDMETHOD(  
   Notify  
)(  
   MMC_NOTIFY_TYPE event,  
   long arg,  
   long param,  
   IComponentData* pComponentData,  
   IComponent* pComponent,  
   DATA_OBJECT_TYPES type  
) = 0;  
```  
  
#### Parameters  
 `event`  
 [in] Identifies an action taken by a user. The following notifications are possible:  
  
-   **MMCN_ACTIVATE** Sent when a window is being activated and deactivated.  
  
-   **MMCN_ADD_IMAGES** Sent to add images to the result pane.  
  
-   **MMCN_BTN_CLICK** Sent when the user clicks one of the toolbar buttons.  
  
-   **MMCN_CLICK** Sent when a user clicks a mouse button on a list view item.  
  
-   **MMCN_DBLCLICK** Sent when a user double clicks a mouse button on a list view item.  
  
-   **MMCN_DELETE** Sent to inform the snap-in that the object should be deleted.  
  
-   **MMCN_EXPAND** Sent when a folder needs to be expanded or contracted.  
  
-   **MMCN_MINIMIZED** Sent when a window is being minimized or maximized.  
  
-   **MMCN_PROPERTY_CHANGE** Sent to notify a snap-in object that the snap-in object's view is about to change.  
  
-   **MMCN_REMOVE_CHILDREN** Sent when the snap-in must delete the entire subtree it has added below the specified node.  
  
-   **MMCN_RENAME** Sent the first time to query for a rename and the second time to do the rename.  
  
-   **MMCN_SELECT** Sent when an item in the scope or result view pane is selected.  
  
-   **MMCN_SHOW** Sent when a scope item is selected or deselected for the first time.  
  
-   **MMCN_VIEW_CHANGE** Sent when the snap-in can update all views when a change occurs.  
  
 `arg`  
 [in] Depends on the notification type.  
  
 `param`  
 [in] Depends on the notification type.  
  
 *pComponentData*  
 [out] A pointer to the object implementing **IComponentData**. This parameter is **NULL** if the notification is not being forwarded from **IComponentData::Notify**.  
  
 *pComponent*  
 [out] A pointer to the object that implements **IComponent**. This parameter is **NULL** if the notification is not being forwarded from **IComponent::Notify**.  
  
 `type`  
 [in] Specifies the type of object. It can have one of the following values:  
  
-   **CCT_SCOPE** Data object for scope pane context.  
  
-   **CCT_RESULT** Data object for result pane context.  
  
-   **CCT_SNAPIN_MANAGER** Data object for snap-in manager context.  
  
-   **CCT_UNINITIALIZED** Data object has an invalid type.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInItemImpl Class](../Topic/CSnapInItemImpl%20Class.md)