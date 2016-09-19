---
title: "CMDIFrameWndEx::GetDefaultResId"
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
ms.assetid: 0a2fde4f-5463-4b35-83b1-15d959eaa550
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::GetDefaultResId
Returns the ID of shared resources of the MDI frame window.  
  
## Syntax  
  
```  
UINT GetDefaultResId() const;  
```  
  
## Return Value  
 A resource ID value. 0 if the frame window has no menu bar.  
  
## Remarks  
 This method returns the resource ID that was specified when the MDI frame window was loaded by [CFrameWnd::LoadFrame](../vs140/CFrameWnd--LoadFrame.md).  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)