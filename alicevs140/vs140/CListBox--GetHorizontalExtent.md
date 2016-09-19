---
title: "CListBox::GetHorizontalExtent"
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
ms.assetid: 47d50ef1-9e16-453b-9e8c-87e6a4df1000
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetHorizontalExtent
Retrieves from the list box the width in pixels by which it can be scrolled horizontally.  
  
## Syntax  
  
```  
  
int GetHorizontalExtent( ) const;  
```  
  
## Return Value  
 The scrollable width of the list box, in pixels.  
  
## Remarks  
 This is applicable only if the list box has a horizontal scroll bar.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#14)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::SetHorizontalExtent](../vs140/CListBox--SetHorizontalExtent.md)   
 [LB_GETHORIZONTALEXTENT](http://msdn.microsoft.com/library/windows/desktop/bb775200)