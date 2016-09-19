---
title: "CDC::DeleteDC"
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
ms.assetid: 6ea981e2-bc44-4380-a380-1b80aebee672
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::DeleteDC
In general, do not call this function; the destructor will do it for you.  
  
## Syntax  
  
```  
  
BOOL DeleteDC( );  
```  
  
## Return Value  
 Nonzero if the function completed successfully; otherwise 0.  
  
## Remarks  
 The `DeleteDC` member function deletes the Windows device contexts that are associated with `m_hDC` in the current `CDC` object. If this `CDC` object is the last active device context for a given device, the device is notified and all storage and system resources used by the device are released.  
  
 An application should not call `DeleteDC` if objects have been selected into the device context. Objects must first be selected out of the device context before it is deleted.  
  
 An application must not delete a device context whose handle was obtained by calling [CWnd::GetDC](../vs140/CWnd--GetDC.md). Instead, it must call [CWnd::ReleaseDC](../vs140/CWnd--ReleaseDC.md) to free the device context. The [CClientDC](../vs140/CClientDC-Class.md) and [CWindowDC](../vs140/CWindowDC-Class.md) classes are provided to wrap this functionality.  
  
 The `DeleteDC` function is generally used to delete device contexts created with [CreateDC](../vs140/CDC--CreateDC.md), [CreateIC](../vs140/CDC--CreateIC.md), or [CreateCompatibleDC](../vs140/CDC--CreateCompatibleDC.md).  
  
## Example  
 See the example for [CPrintDialog::GetPrinterDC](../vs140/CPrintDialog--GetPrinterDC.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::CDC](../vs140/CDC--CDC.md)   
 [DeleteDC](http://msdn.microsoft.com/library/windows/desktop/dd183533)   
 [CDC::CreateDC](../vs140/CDC--CreateDC.md)   
 [CDC::CreateIC](../vs140/CDC--CreateIC.md)   
 [CDC::CreateCompatibleDC](../vs140/CDC--CreateCompatibleDC.md)   
 [CWnd::GetDC](../vs140/CWnd--GetDC.md)   
 [CWnd::ReleaseDC](../vs140/CWnd--ReleaseDC.md)