---
title: "CDocTemplate::SetServerInfo"
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
ms.assetid: 4cff62bd-5fc1-4f8c-a760-be95afab9bba
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::SetServerInfo
Determines the resources and classes when the server document is embedded or edited in-place.  
  
## Syntax  
  
```  
  
      void SetServerInfo(  
   UINT nIDOleEmbedding,  
   UINT nIDOleInPlaceServer = 0,  
   CRuntimeClass* pOleFrameClass = NULL,  
   CRuntimeClass* pOleViewClass = NULL   
);  
```  
  
#### Parameters  
 *nIDOleEmbedding*  
 The ID of the resources used when an embedded object is opened in a separate window.  
  
 `nIDOleInPlaceServer`  
 The ID of the resources used when an embedded object is activated in-place.  
  
 *pOleFrameClass*  
 Pointer to a [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) structure containing class information for the frame window object created when in-place activation occurs.  
  
 *pOleViewClass*  
 Pointer to a `CRuntimeClass` structure containing class information for the view object created when in-place activation occurs.  
  
## Remarks  
 Call this member function to identify resources that will be used by the server application when the user requests activation of an embedded object. These resources consist of menus and accelerator tables. This function is usually called in the `InitInstance` of your application.  
  
 The menu associated with `nIDOleInPlaceServer` contains separators that allow the server menu to merge with the menu of the container. For more information about merging server and container menus, see the article [Menus and Resources (OLE)](../vs140/Menus-and-Resources--OLE-.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMultiDocTemplate::CMultiDocTemplate](../vs140/CMultiDocTemplate--CMultiDocTemplate.md)   
 [CDocTemplate::SetContainerInfo](../vs140/CDocTemplate--SetContainerInfo.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)