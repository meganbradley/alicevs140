---
title: "COleDispatchDriver::m_lpDispatch"
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
ms.assetid: 36d8d410-5c98-4858-99ac-8a87c77d2b7c
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchDriver::m_lpDispatch
The pointer to the `IDispatch` interface attached to this `COleDispatchDriver`.  
  
## Syntax  
  
```  
  
LPDISPATCH m_lpDispatch;  
  
```  
  
## Remarks  
 The `m_lpDispatch` data member is a public variable of type `LPDISPATCH`.  
  
 For more information, see [IDispatch](assetId:///0e171f7f-0022-4e9b-ac8e-98192828e945) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [COleDispatchDriver::AttachDispatch](../vs140/COleDispatchDriver--AttachDispatch.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDispatchDriver::AttachDispatch](../vs140/COleDispatchDriver--AttachDispatch.md)   
 [COleDispatchDriver::ReleaseDispatch](../vs140/COleDispatchDriver--ReleaseDispatch.md)   
 [COleDispatchDriver::CreateDispatch](../vs140/COleDispatchDriver--CreateDispatch.md)   
 [COleDispatchDriver::DetachDispatch](../vs140/COleDispatchDriver--DetachDispatch.md)