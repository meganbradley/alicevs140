---
title: "CDocObjectServer::OnSaveViewState"
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
ms.assetid: 589689e6-f2df-4e64-b6d4-f2e8416c6b4a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocObjectServer::OnSaveViewState
Override this function to save extra state information about your DocObject view.  
  
## Syntax  
  
```  
  
      virtual void OnSaveViewState(  
   CArchive& ar   
);  
```  
  
#### Parameters  
 `ar`  
 A `CArchive` object to which the view state is serialized.  
  
## Remarks  
 Your state might include properties like the view type, zoom factor, insertion and selection point, and so on. The container typically calls this function before deactivating the view. The saved state can later be restored through [OnApplyViewState](../vs140/CDocObjectServer--OnApplyViewState.md).  
  
 You can use `OnSaveViewState` to store persistent information specific to your view's state. If you override `OnSaveViewState` to store information, you will want to override `OnApplyViewState` to read that information and apply it to your view when it is newly activated.  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [CDocObjectServer Class](../vs140/CDocObjectServer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServer::OnApplyViewState](../vs140/CDocObjectServer--OnApplyViewState.md)