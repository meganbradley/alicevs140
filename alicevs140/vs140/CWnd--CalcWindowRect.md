---
title: "CWnd::CalcWindowRect"
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
ms.assetid: a40592c4-9cd7-4810-9ad0-ea69b98ac1a9
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::CalcWindowRect
Calculates the window rectangle that can contain the specified client rectangle.  
  
## Syntax  
  
```  
virtual void CalcWindowRect(  
   LPRECT lpClientRect,  
   UINT nAdjustType = adjustBorder   
);  
```  
  
#### Parameters  
 [in, out] `lpClientRect`  
 Pointer to a rectangle structure. On input, this structure contains the client rectangle. After the method is finished, this structure contains the window rectangle that can contain the specified client rectangle.  
  
 [in] `nAdjustType`  
 Use `CWnd::adjustBorder` to calculate window coordinates without the `WS_EX_CLIENTEDGE` style; otherwise, use `CWnd::adjustOutside`.  
  
## Remarks  
 The size of the calculated window rectangle does not include space for a menu bar.  
  
 For more usage restrictions, see [AdjustWindowRectEx](http://msdn.microsoft.com/library/windows/desktop/ms632667).  
  
## Example  
 [!CODE [NVC_MFCWindowing#72](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#72)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [AdjustWindowRectEx](http://msdn.microsoft.com/library/windows/desktop/ms632667)