---
title: "CMFCToolBar::OnChangeHot"
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
ms.assetid: 578b9550-db41-4b19-a6fb-b5a2b8127efd
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::OnChangeHot
Called by the framework when a user selects a button on the toolbar.  
  
## Syntax  
  
```  
virtual void OnChangeHot(  
   int iHot   
);  
```  
  
#### Parameters  
 [in] `iHot`  
 Specifies the index of the toolbar button that is selected; or -1 if no toolbar button is selected.  
  
## Remarks  
 Override this method to process notifications that the user selected a button on a toolbar.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)