---
title: "Current Selection in a Rich Edit Control"
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
ms.topic: article
ms.assetid: f6b2a2b6-5481-4ad3-9720-6dd772ea6fc8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Current Selection in a Rich Edit Control
The user can select text in a rich edit control ([CRichEditCtrl](../vs140/CRichEditCtrl-Class.md)) by using the mouse or the keyboard. The current selection is the range of selected characters, or the position of the insertion point if no characters are selected. An application can get information about the current selection, set the current selection, determine when the current selection changes, and show or hide the selection highlight.  
  
 To determine the current selection in a rich edit control, use the [GetSel](../vs140/CRichEditCtrl--GetSel.md) member function. To set the current selection, use the [SetSel](../vs140/CRichEditCtrl--SetSel.md) member function. The [CHARRANGE](http://msdn.microsoft.com/library/windows/desktop/bb787885) structure is used with these functions to specify a range of characters. To retrieve information about the contents of the current selection, you can use the [GetSelectionType](../vs140/CRichEditCtrl--GetSelectionType.md) member function.  
  
 By default, a rich edit control shows and hides the selection highlight when it gains and loses the focus. You can show or hide the selection highlight at any time by using the [HideSelection](../vs140/CRichEditCtrl--HideSelection.md) member function. For example, an application might provide a Search dialog box to find text in a rich edit control. The application might select matching text without closing the dialog box, in which case it must use `HideSelection` to highlight the selection.  
  
 To get the selected text in a rich edit control, use the [GetSelText](../vs140/CRichEditCtrl--GetSelText.md) member function. The text is copied to the specified character array. You must ensure that the array is large enough to hold the selected text plus a terminating null character.  
  
 You can search for a string in a rich edit control by using the [FindText](../vs140/CRichEditCtrl--FindText.md) member function The [FINDTEXTEX](http://msdn.microsoft.com/library/windows/desktop/bb787909) structure used with this function specifies the text range to search and the string to search for. You can also specify such options as whether the search is case-sensitive.  
  
## See Also  
 [Using CRichEditCtrl](../vs140/Using-CRichEditCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)