---
title: "CSplitterWnd::DeleteColumn"
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
ms.assetid: dcd33ada-1b17-425e-bc74-12ddd1abd298
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::DeleteColumn
Deletes a column from the splitter window.  
  
## Syntax  
  
```  
  
      virtual void DeleteColumn(  
   int colDelete   
);  
```  
  
#### Parameters  
 *colDelete*  
 Specifies the column to be deleted.  
  
## Remarks  
 This member function is called by the framework to implement the logic of the dynamic splitter window (that is, if the splitter window has the **SPLS_DYNAMIC_SPLIT** style). It can be customized, along with the virtual function [CreateView](../vs140/CSplitterWnd--CreateView.md), to implement more advanced dynamic splitters.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::DeleteRow](../vs140/CSplitterWnd--DeleteRow.md)   
 [CSplitterWnd::CreateView](../vs140/CSplitterWnd--CreateView.md)   
 [CSplitterWnd::DeleteView](../vs140/CSplitterWnd--DeleteView.md)