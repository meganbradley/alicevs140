---
title: "CPagerCtrl::GetDropTarget"
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
ms.assetid: 1ee01946-edd6-4c3c-98c9-8687f52d5357
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPagerCtrl::GetDropTarget
Retrieves the [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679) interface for the current pager control.  
  
## Syntax  
  
```  
IDropTarget* GetDropTarget() const;  
```  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Return Value  
 A pointer to the `IDropTarget` interface for the current pager control.  
  
## Remarks  
 `IDropTarget` is one of the interfaces you implement to support drag-and-drop operations in your application.  
  
 This method sends the [PGM_GETDROPTARGET](http://msdn.microsoft.com/library/windows/desktop/bb760872) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The caller of this method is responsible for calling the `Release` member of the [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679) interface when the interface is no longer needed.  
  
## See Also  
 [CPagerCtrl Class](../vs140/CPagerCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [PGM_GETDROPTARGET](http://msdn.microsoft.com/library/windows/desktop/bb760872)   
 [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679)