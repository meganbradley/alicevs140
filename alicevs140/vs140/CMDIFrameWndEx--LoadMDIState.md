---
title: "CMDIFrameWndEx::LoadMDIState"
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
ms.assetid: 1fdd209d-0fdf-41db-a7c9-c4f56de442d3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::LoadMDIState
Loads the specified layout of MDI Tabbed Groups and the list of previously opened documents.  
  
## Syntax  
  
```  
virtual BOOL LoadMDIState(  
   LPCTSTR lpszProfileName   
);  
```  
  
#### Parameters  
 [in] `lpszProfileName`  
 Specifies the profile name.  
  
## Return Value  
 `TRUE` if the load succeeded; `FALSE` if the load failed or there is no data to load.  
  
## Remarks  
 To load or save the state of MDI tabs and groups and the list of opened documents, do the following:  
  
-   Call [CMDIFrameWndEx::SaveMDIState](../vs140/CMDIFrameWndEx--SaveMDIState.md) when the main frame is being closed  
  
-   Call [CMDIFrameWndEx::LoadMDIState](../vs140/CMDIFrameWndEx--LoadMDIState.md) when the main frame is being created. The recommended place for this call is before the main frame is displayed for the first time. Add `CWinAppEx::EnableLoadWindowPlacement` `(FALSE);` before `pMainFrame->LoadFrame (IDR_MAINFRAME);.` Add `CBCGPWorkspace::ReloadWindowPlacement` `(pMainFrame);` after the call to `LoadMDIState` to display the main frame at the position that was stored in the registry.  
  
-   Override `GetDocumentName` in the `CMDIChildWndEx`- derived class if your application displays documents that are not stored as files. The returned string will be saved in the registry as the document identifier. The base implementation of [CMDIChildWndEx::GetDocumentName](../vs140/CMDIChildWndEx--GetDocumentName.md) returns a value obtained from [CDocument::GetPathName](../vs140/CDocument--GetPathName.md).  
  
-   Override [CMDIFrameWndEx::CreateDocumentWindow](../vs140/CMDIFrameWndEx--CreateDocumentWindow.md) to correctly create documents when they are being loaded from the registry. The first parameter is the string that `GetDocumentName` returned.  
  
## Example  
 The following example shows how `LoadMDIState` is used in the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#11](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#11)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)