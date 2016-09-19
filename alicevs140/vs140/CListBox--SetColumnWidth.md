---
title: "CListBox::SetColumnWidth"
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
ms.assetid: 1a2e352e-79d8-4b0a-b6c4-407a2dc23058
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetColumnWidth
Sets the width in pixels of all columns in a multicolumn list box (created with the [LBS_MULTICOLUMN](../vs140/List-Box-Styles.md) style).  
  
## Syntax  
  
```  
  
      void SetColumnWidth(  
   int cxWidth   
);  
```  
  
#### Parameters  
 `cxWidth`  
 Specifies the width in pixels of all columns.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#31](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#31)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_SETCOLUMNWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb761338)