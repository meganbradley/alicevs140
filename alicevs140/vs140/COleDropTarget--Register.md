---
title: "COleDropTarget::Register"
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
ms.assetid: 6eb7df4b-a1d6-480a-8d08-5b2313392c05
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDropTarget::Register
Call this function to register your window with the OLE DLLs as a valid drop target.  
  
## Syntax  
  
```  
  
      BOOL Register(  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `pWnd`  
 Points to the window that is to be registered as a drop target.  
  
## Return Value  
 Nonzero if registration is successful; otherwise 0.  
  
## Remarks  
 This function must be called for drop operations to be accepted.  
  
 For more information, see [RegisterDragDrop](http://msdn.microsoft.com/library/windows/desktop/ms678405) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDropTarget Class](../vs140/COleDropTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDropTarget::Revoke](../vs140/COleDropTarget--Revoke.md)   
 [COleDropTarget::COleDropTarget](../vs140/COleDropTarget--COleDropTarget.md)