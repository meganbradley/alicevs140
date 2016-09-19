---
title: "CListBox::CharToItem"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: f4f454ff-0828-4cce-9cf0-38487c1b6cfe
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::CharToItem
Called by the framework when the list box's parent window receives a `WM_CHARTOITEM` message from the list box.  
  
## Syntax  
  
```  
  
      virtual int CharToItem(  
   UINT nKey,  
   UINT nIndex   
);  
```  
  
#### Parameters  
 `nKey`  
 The ANSI code of the character the user typed.  
  
 `nIndex`  
 The current position of the list-box caret.  
  
## Return Value  
 Returns – 1 or – 2 for no further action or a nonnegative number to specify an index of a list-box item on which to perform the default action for the keystroke. The default implementation returns – 1.  
  
## Remarks  
 The `WM_CHARTOITEM` message is sent by the list box when it receives a `WM_CHAR` message, but only if the list box meets all of these criteria:  
  
-   Is an owner-draw list box.  
  
-   Does not have the [LBS_HASSTRINGS](../vs140/List-Box-Styles.md) style set.  
  
-   Has at least one item.  
  
 You should never call this function yourself. Override this function to provide your own custom handling of keyboard messages.  
  
 In your override, you must return a value to tell the framework what action you performed. A return value of – 1 or – 2 indicates that you handled all aspects of selecting the item and requires no further action by the list box. Before returning – 1 or – 2, you could set the selection or move the caret or both. To set the selection, use [SetCurSel](../vs140/CListBox--SetCurSel.md) or [SetSel](../vs140/CListBox--SetSel.md). To move the caret, use [SetCaretIndex](../vs140/CListBox--SetCaretIndex.md).  
  
 A return value of 0 or greater specifies the index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the given item.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#4)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::VKeyToItem](../vs140/CListBox--VKeyToItem.md)   
 [CListBox::SetCurSel](../vs140/CListBox--SetCurSel.md)   
 [CListBox::SetSel](../vs140/CListBox--SetSel.md)   
 [CListBox::SetCaretIndex](../vs140/CListBox--SetCaretIndex.md)   
 [WM_CHARTOITEM](http://msdn.microsoft.com/library/windows/desktop/bb761358)