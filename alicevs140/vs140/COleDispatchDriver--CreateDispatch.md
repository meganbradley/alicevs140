---
title: "COleDispatchDriver::CreateDispatch"
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
ms.assetid: fad59519-ffd5-42f2-982e-f50f40054f93
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchDriver::CreateDispatch
Creates an [IDispatch](assetId:///0e171f7f-0022-4e9b-ac8e-98192828e945) interface object and attaches it to the `COleDispatchDriver` object.  
  
## Syntax  
  
```  
  
BOOL CreateDispatch(  
		REFCLSID clsid,  
		COleException* pError = NULL  
		);  
  
BOOL CreateDispatch(  
    LPCTSTR lpszProgID,  
    COleException* pError = NULL   
    );  
```  
  
#### Parameters  
 `clsid`  
 Class ID of the `IDispatch` connection object to be created.  
  
 `pError`  
 Pointer to an OLE exception object, which will hold the status code resulting from the creation.  
  
 `lpszProgID`  
 Pointer to the programmatic identifier, such as "Excel.Document.5", of the automation object for which the dispatch object is to be created.  
  
## Return Value  
 Nonzero on success; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#4)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDispatchDriver::DetachDispatch](../vs140/COleDispatchDriver--DetachDispatch.md)   
 [COleDispatchDriver::ReleaseDispatch](../vs140/COleDispatchDriver--ReleaseDispatch.md)   
 [COleDispatchDriver::AttachDispatch](../vs140/COleDispatchDriver--AttachDispatch.md)   
 [COleException Class](../vs140/COleException-Class.md)   
 [COleDispatchDriver::m_lpDispatch](../vs140/COleDispatchDriver--m_lpDispatch.md)