---
title: "CWnd::GetUpdateRgn"
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
ms.assetid: 97c76292-e274-46f2-9ba7-78264d0f9101
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetUpdateRgn
Retrieves the update region into a region identified by `pRgn`.  
  
## Syntax  
  
```  
  
      int GetUpdateRgn(  
   CRgn* pRgn,  
   BOOL bErase = FALSE   
);  
```  
  
#### Parameters  
 `pRgn`  
 Identifies the update region.  
  
 `bErase`  
 Specifies whether the background will be erased and nonclient areas of child windows will be drawn. If the value is **FALSE**, no drawing is done.  
  
## Return Value  
 Specifies a short-integer flag that indicates the type of resulting region. The value can take any one of the following:  
  
-   **SIMPLEREGION** The region has no overlapping borders.  
  
-   **COMPLEXREGION** The region has overlapping borders.  
  
-   **NULLREGION** The region is empty.  
  
-   **ERROR** No region was created.  
  
## Remarks  
 The coordinates of this region are relative to the upper-left corner (client coordinates).  
  
 The [BeginPaint](../vs140/CWnd--BeginPaint.md) member function automatically validates the update region, so any call to `GetUpdateRgn` made immediately after a call to `BeginPaint` retrieves an empty update region.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::BeginPaint](../vs140/CWnd--BeginPaint.md)   
 [GetUpdateRgn](http://msdn.microsoft.com/library/windows/desktop/dd144944)