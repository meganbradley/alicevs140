---
title: "CListBox::VKeyToItem"
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
ms.assetid: 49fcd057-8ce0-4342-a99d-e3d2512b7981
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::VKeyToItem
Called by the framework when the list box's parent window receives a `WM_VKEYTOITEM` message from the list box.  
  
## Syntax  
  
```  
  
      virtual int VKeyToItem(  
   UINT nKey,  
   UINT nIndex   
);  
```  
  
#### Parameters  
 `nKey`  
 The virtual key code of the key the user pressed. For a list of of standard virtual key codes, see Winuser.h  
  
 `nIndex`  
 The current position of the list-box caret.  
  
## Return Value  
 Returns – 2 for no further action, – 1 for default action, or a nonnegative number to specify an index of a list box item on which to perform the default action for the keystroke.  
  
## Remarks  
 The `WM_VKEYTOITEM` message is sent by the list box when it receives a `WM_KEYDOWN` message, but only if the list box meets both of the following:  
  
-   Has the [LBS_WANTKEYBOARDINPUT](../vs140/List-Box-Styles.md) style set.  
  
-   Has at least one item.  
  
 You should never call this function yourself. Override this function to provide your own custom handling of keyboard messages.  
  
 You must return a value to tell the framework what action your override performed. A return value of – 2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box. Before returning – 2, you could set the selection or move the caret or both. To set the selection, use [SetCurSel](../vs140/CListBox--SetCurSel.md) or [SetSel](../vs140/CListBox--SetSel.md). To move the caret, use [SetCaretIndex](../vs140/CListBox--SetCaretIndex.md).  
  
 A return value of – 1 indicates that the list box should perform the default action in response to the keystroke.The default implementation returns – 1.  
  
 A return value of 0 or greater specifies the index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the given item.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#41](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#41)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::CharToItem](../vs140/CListBox--CharToItem.md)   
 [CListBox::SetCurSel](../vs140/CListBox--SetCurSel.md)   
 [CListBox::SetSel](../vs140/CListBox--SetSel.md)   
 [CListBox::SetCaretIndex](../vs140/CListBox--SetCaretIndex.md)