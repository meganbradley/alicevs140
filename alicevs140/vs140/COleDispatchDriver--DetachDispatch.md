---
title: "COleDispatchDriver::DetachDispatch"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: c4a4365d-74eb-4139-9f1b-d7588ad73dcb
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchDriver::DetachDispatch
Detaches the current `IDispatch` connection from this object.  
  
## Syntax  
  
```  
  
LPDISPATCH DetachDispatch( );  
```  
  
## Return Value  
 A pointer to the previously attached OLE `IDispatch` object.  
  
## Remarks  
 The `IDispatch` is not released.  
  
 For more information about the `LPDISPATCH` type, see [Implementing the IDispatch Interface](assetId:///0e171f7f-0022-4e9b-ac8e-98192828e945) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCOleContainer#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#5)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDispatchDriver::ReleaseDispatch](../vs140/COleDispatchDriver--ReleaseDispatch.md)   
 [COleDispatchDriver::CreateDispatch](../vs140/COleDispatchDriver--CreateDispatch.md)   
 [COleDispatchDriver::AttachDispatch](../vs140/COleDispatchDriver--AttachDispatch.md)   
 [COleDispatchDriver::m_lpDispatch](../vs140/COleDispatchDriver--m_lpDispatch.md)