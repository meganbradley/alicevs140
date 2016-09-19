---
title: "CHtmlView::OnFrameWindowActivate"
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
ms.assetid: a9b2e480-45d3-496c-8d01-56f4bd9ccd9c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnFrameWindowActivate
Called from [IOleInPlaceActiveObject::OnFrameWindowActivate](http://msdn.microsoft.com/library/windows/desktop/ms683969) to notify the object when the container's top-level frame window is activated or deactivated.  
  
## Syntax  
  
```  
  
      virtual HRESULT OnFrameWindowActivate(  
   BOOL fActivate   
);  
```  
  
#### Parameters  
 `fActivate`  
 Indicates the state of the container's top-level frame window. If this value is nonzero, the window is being activated. If this value is zero, the window is being deactivated.  
  
## Return Value  
 `S_OK` if successful, or an OLE-defined error code otherwise.  
  
## Remarks  
 Override `OnFrameWindowActivate` to react to the `OnFrameWindowActivate` notification from the Microsoft Web Browser control. See [IDocHostUIHandler::OnFrameWindowActivate](https://msdn.microsoft.com/en-us/library/aa753262.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)