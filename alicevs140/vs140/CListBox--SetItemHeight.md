---
title: "CListBox::SetItemHeight"
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
ms.assetid: 1d255403-79ea-4130-a799-3b8fdab408d8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetItemHeight
Sets the height of items in a list box.  
  
## Syntax  
  
```  
  
      int SetItemHeight(  
   int nIndex,  
   UINT cyItemHeight   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the item in the list box. This parameter is used only if the list box has the **LBS_OWNERDRAWVARIABLE** style; otherwise, it should be set to 0.  
  
 `cyItemHeight`  
 Specifies the height, in pixels, of the item.  
  
## Return Value  
 **LB_ERR** if the index or height is invalid.  
  
## Remarks  
 If the list box has the [LBS_OWNERDRAWVARIABLE](../vs140/List-Box-Styles.md) style, this function sets the height of the item specified by `nIndex`. Otherwise, this function sets the height of all items in the list box.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#36)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::GetItemHeight](../vs140/CListBox--GetItemHeight.md)   
 [LB_SETITEMHEIGHT](http://msdn.microsoft.com/library/windows/desktop/bb761348)