---
title: "CDocTemplate::SetContainerInfo"
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
ms.assetid: fc4cd027-4ee9-406a-8c00-994950f4e525
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::SetContainerInfo
Determines the resources for OLE containers when editing an in-place OLE item.  
  
## Syntax  
  
```  
  
      void SetContainerInfo(  
   UINT nIDOleInPlaceContainer   
);  
```  
  
#### Parameters  
 `nIDOleInPlaceContainer`  
 The ID of the resources used when an embedded object is activated.  
  
## Remarks  
 Call this function to set the resources to be used when an OLE object is in-place activated. These resources may include menus and accelerator tables. This function is usually called in the [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md) function of your application.  
  
 The menu associated with `nIDOleInPlaceContainer` contains separators that allow the menu of the activated in-place item to merge with the menu of the container application. For more information about merging server and container menus, see the article [Menus and Resources (OLE)](../vs140/Menus-and-Resources--OLE-.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate::SetServerInfo](../vs140/CDocTemplate--SetServerInfo.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)   
 [CMultiDocTemplate::CMultiDocTemplate](../vs140/CMultiDocTemplate--CMultiDocTemplate.md)