---
title: "COleDispatchDriver::m_bAutoRelease"
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
ms.assetid: 0a07fc46-a136-40a7-b8b1-8849cf0792d6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchDriver::m_bAutoRelease
If **TRUE**, the COM object accessed by [m_lpDispatch](../vs140/COleDispatchDriver--m_lpDispatch.md) will be automatically released when [ReleaseDispatch](../vs140/COleDispatchDriver--ReleaseDispatch.md) is called or when this `COleDispatchDriver` object is destroyed.  
  
## Syntax  
  
```  
  
BOOL m_bAutoRelease;  
  
```  
  
## Remarks  
 By default, `m_bAutoRelease` is set to **TRUE** in the constructor.  
  
 For more information on releasing COM objects, see [Implementing Reference Counting](http://msdn.microsoft.com/library/windows/desktop/ms693431) and [IUnknown::Release](http://msdn.microsoft.com/library/windows/desktop/ms682317) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCOleContainer#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#9)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleDispatchDriver Class](../vs140/COleDispatchDriver-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDispatchDriver::AttachDispatch](../vs140/COleDispatchDriver--AttachDispatch.md)   
 [COleDispatchDriver::ReleaseDispatch](../vs140/COleDispatchDriver--ReleaseDispatch.md)   
 [COleDispatchDriver::m_lpDispatch](../vs140/COleDispatchDriver--m_lpDispatch.md)