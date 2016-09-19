---
title: "CHtmlView::OnDocWindowActivate"
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
ms.assetid: 2976c341-9b0e-4384-9e83-863839385bb1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnDocWindowActivate
Called from the Internet Explorer or MSHTML implementation of **IOleInPlaceActiveObject::OnDocWindowActivate**, which notifies the active in-place object when the container's document window is activated or deactivated.  
  
## Syntax  
  
```  
  
      virtual HRESULT OnDocWindowActivate(  
   BOOL fActivate   
);  
```  
  
#### Parameters  
 `fActivate`  
 Indicates the state of the document window. If this value is nonzero, the window is being activated. If this value is zero, the window is being deactivated.  
  
## Return Value  
 `S_OK` if successful, or an OLE-defined error code otherwise.  
  
## Remarks  
 Override `OnDocWindowActivate` to react to the `OnDocWindowActivate` notification from the Microsoft Web Browser control. See [IDocHostUIHandler::OnDocWindowActivate](https://msdn.microsoft.com/en-us/library/aa753261.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IOleInPlaceActiveObject::OnDocWindowActivate](http://msdn.microsoft.com/library/windows/desktop/ms687281)