---
title: "CHtmlView::OnGetDropTarget"
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
ms.assetid: bbda20d2-31d2-4e19-b149-95f110e85479
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnGetDropTarget
Called by Internet Explorer or MSHTML when it is being used as a drop target to allow the host to supply an alternative `IDropTarget`.  
  
## Syntax  
  
```  
  
      virtual HRESULT OnGetDropTarget(  
   LPDROPTARGET pDropTarget,  
   LPDROPTARGET* ppDropTarget   
);  
```  
  
#### Parameters  
 `pDropTarget`  
 [IDropTarget](http://msdn.microsoft.com/library/windows/desktop/ms679679) Internet Explorer or MSHTML proposes to use.  
  
 `ppDropTarget`  
 Address of the `IDropTarget` that receives the `IDropTarget` interface pointer the host wants to provide.  
  
## Return Value  
 See [IDocHostUIHandler::GetDropTarget](https://msdn.microsoft.com/en-us/library/aa753255.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a list of return codes.  
  
## Remarks  
 Override `OnGetDropTarget` to react to the `GetDropTarget` notification from the Microsoft Web Browser control. See [IDocHostUIHandler::GetDropTarget](https://msdn.microsoft.com/en-us/library/aa753255.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)