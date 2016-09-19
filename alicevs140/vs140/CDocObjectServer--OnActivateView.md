---
title: "CDocObjectServer::OnActivateView"
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
ms.assetid: ade4fed1-b20d-49de-bd80-2176d87b159f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocObjectServer::OnActivateView
Call this function to display the DocObject view.  
  
## Syntax  
  
```  
  
virtual HRESULT OnActivateView( );  
```  
  
## Return Value  
 Returns an error or warning value. By default, returns **NOERROR** if successful; otherwise, **E_FAIL**.  
  
## Remarks  
 This function creates an in-place frame window, draws scrollbars within the view, sets up the menus the server shares with its container, adds frame controls, sets the active object, then finally shows the in-place frame window and sets the focus.  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [CDocObjectServer Class](../vs140/CDocObjectServer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServer::OnApplyViewState](../vs140/CDocObjectServer--OnApplyViewState.md)