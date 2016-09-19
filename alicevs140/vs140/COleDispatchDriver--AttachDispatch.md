---
title: "COleDispatchDriver::AttachDispatch"
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
ms.assetid: 9765d01c-1f3f-4f31-be32-14dc5f44c263
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchDriver::AttachDispatch
Call the `AttachDispatch` member function to attach an `IDispatch` pointer to the `COleDispatchDriver` object. For more information, see [Implementing the IDispatch Interface](assetId:///0e171f7f-0022-4e9b-ac8e-98192828e945).  
  
## Syntax  
  
```  
void AttachDispatch(  
		LPDISPATCH lpDispatch,  
		BOOLbAutoRelease = TRUE  
		);  
```  
  
#### Parameters  
 `lpDispatch`  
 Pointer to an OLE `IDispatch` object to be attached to the `COleDispatchDriver` object.  
  
 `bAutoRelease`  
 Specifies whether the dispatch is to be released when this object goes out of scope.  
  
## Remarks  
 This function releases any `IDispatch` pointer that is already attached to the `COleDispatchDriver` object.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#3)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDispatchDriver::DetachDispatch](../vs140/COleDispatchDriver--DetachDispatch.md)   
 [COleDispatchDriver::ReleaseDispatch](../vs140/COleDispatchDriver--ReleaseDispatch.md)   
 [COleDispatchDriver::CreateDispatch](../vs140/COleDispatchDriver--CreateDispatch.md)   
 [COleDispatchDriver::m_lpDispatch](../vs140/COleDispatchDriver--m_lpDispatch.md)   
 [COleDispatchDriver::m_bAutoRelease](../vs140/COleDispatchDriver--m_bAutoRelease.md)