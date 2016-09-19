---
title: "CSplitterWnd::IsChildPane"
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
ms.assetid: 1cdffbed-03f2-41ae-a173-16731c2be4ae
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::IsChildPane
Determines whether `pWnd` is currently a child pane of this splitter window.  
  
## Syntax  
  
```  
  
      BOOL IsChildPane(  
   CWnd* pWnd,  
   int* pRow,  
   int* pCol  
);  
```  
  
#### Parameters  
 `pWnd`  
 A pointer to a [CWnd](../vs140/CWnd-Class.md) object to be tested.  
  
 `pRow`  
 A pointer to an `int` in which to store row number.  
  
 `pCol`  
 A pointer to an `int` in which to store a column number.  
  
## Return Value  
 If nonzero, `pWnd` is currently a child pane of this splitter window, and `pRow` and `pCol` are filled in with the position of the pane in the splitter window. If `pWnd` is not a child pane of this splitter window, 0 is returned.  
  
## Remarks  
 In Visual C++ versions prior to 6.0, this function was defined as  
  
 `BOOL IsChildPane(CWnd* pWnd, int& row, int& col);`  
  
 This version is now obsolete and should not be used.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::GetPane](../vs140/CSplitterWnd--GetPane.md)