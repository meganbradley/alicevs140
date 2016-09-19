---
title: "COleControl::GetWindowlessDropTarget"
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
ms.assetid: 9c96a7b1-cfba-4220-97ed-91a09531d736
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetWindowlessDropTarget
Override `GetWindowlessDropTarget` when you want a windowless control to be the target of an OLE drag and drop operation.  
  
## Syntax  
  
```  
  
virtual IDropTarget* GetWindowlessDropTarget( );  
```  
  
## Return Value  
 Pointer to the object's `IDropTarget` interface. Since it does not have a window, a windowless object cannot register an `IDropTarget` interface. However, to participate in drag and drop, a windowless object can still implement the interface and return it in `GetWindowlessDropTarget`.  
  
## Remarks  
 Normally, this would require that the control's window be registered as a drop target. But since the control has no window of its own, the container will use its own window as a drop target. The control simply needs to provide an implementation of the `IDropTarget` interface to which the container can delegate calls at the appropriate time. For example:  
  
 [!CODE [NVC_MFCAxCtl#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAxCtl#2)]  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)