---
title: "CListBox::GetItemHeight"
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
ms.assetid: 5bc2c9f6-8119-42de-a0a2-7e519d5bc112
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetItemHeight
Determines the height of items in a list box.  
  
## Syntax  
  
```  
  
      int GetItemHeight(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the item in the list box. This parameter is used only if the list box has the **LBS_OWNERDRAWVARIABLE** style; otherwise, it should be set to 0.  
  
## Return Value  
 The height, in pixels, of the items in the list box. If the list box has the [LBS_OWNERDRAWVARIABLE](../vs140/List-Box-Styles.md) style, the return value is the height of the item specified by `nIndex`. If an error occurs, the return value is **LB_ERR**.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#17)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_GETITEMHEIGHT](http://msdn.microsoft.com/library/windows/desktop/bb775204)   
 [CListBox::SetItemHeight](../vs140/CListBox--SetItemHeight.md)