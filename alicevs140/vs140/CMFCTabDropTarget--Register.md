---
title: "CMFCTabDropTarget::Register"
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
ms.assetid: 2683f8cf-b896-4935-9085-b08e4bc394c0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabDropTarget::Register
Registers the control as one that can be the target of an OLE drag-and-drop operation.  
  
## Syntax  
  
```  
BOOL Register(CMFCBaseTabCtrl *pOwner);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pOwner`|The tab control to register as a drop target.|  
  
## Return Value  
 Nonzero if registration was successful; otherwise 0.  
  
## Remarks  
 This method calls [COleDropTarget::Register](../vs140/COleDropTarget--Register.md) to register the control for drag-and-drop operations.  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCTabDropTarget Class](../vs140/CMFCTabDropTarget-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [COleDropTarget::Register](../vs140/COleDropTarget--Register.md)