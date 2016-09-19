---
title: "CWnd::SetRedraw"
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
ms.assetid: f3bebab9-7787-44c4-b93f-62f91786e586
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetRedraw
An application calls `SetRedraw` to allow changes to be redrawn or to prevent changes from being redrawn.  
  
## Syntax  
  
```  
  
      void SetRedraw(  
   BOOL bRedraw = TRUE   
);  
```  
  
#### Parameters  
 `bRedraw`  
 Specifies the state of the redraw flag. If this parameter is **TRUE**, the redraw flag is set; if **FALSE**, the flag is cleared.  
  
## Remarks  
 This member function sets or clears the redraw flag. While the redraw flag is cleared, the contents will not be updated after each change and will not be repainted until the redraw flag is set. For example, an application that needs to add several items to a list box can clear the redraw flag, add the items, and then set the redraw flag. Finally, the application can call the [Invalidate](../vs140/CWnd--Invalidate.md) or [InvalidateRect](../vs140/CWnd--InvalidateRect.md) member function to cause the list box to be repainted.  
  
## Example  
 [!CODE [NVC_MFCWindowing#117](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#117)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_SETREDRAW](http://msdn.microsoft.com/library/windows/desktop/dd145219)