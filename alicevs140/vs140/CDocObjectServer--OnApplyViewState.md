---
title: "CDocObjectServer::OnApplyViewState"
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
ms.assetid: b37d6035-fce7-4815-9d9f-7b140301e513
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocObjectServer::OnApplyViewState
Override this function to restore the state of the DocObject view.  
  
## Syntax  
  
```  
  
      virtual void OnApplyViewState(  
   CArchive& ar   
);  
```  
  
#### Parameters  
 `ar`  
 A `CArchive` object from which to serialize the view state.  
  
## Remarks  
 This function is called when the view is being displayed for the first time after its instantiation. `OnApplyViewState` instructs a view to reinitialize itself according to the data in the `CArchive` object previously saved with [OnSaveViewState](../vs140/CDocObjectServer--OnSaveViewState.md). The view must validate the data in the `CArchive` object because the container does not attempt to interpret the view state data in any way.  
  
 You can use `OnSaveViewState` to store persistent information specific to your view's state. If you override `OnSaveViewState` to store information, you will want to override `OnApplyViewState` to read that information and apply it to your view when it is newly activated.  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [CDocObjectServer Class](../vs140/CDocObjectServer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServer::OnSaveViewState](../vs140/CDocObjectServer--OnSaveViewState.md)