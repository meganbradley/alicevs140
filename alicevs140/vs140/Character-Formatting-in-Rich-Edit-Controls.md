---
title: "Character Formatting in Rich Edit Controls"
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
ms.assetid: c80f4305-75ad-45f9-8d17-d83d0fe79be5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Character Formatting in Rich Edit Controls
You can use member functions of the rich edit control ([CRichEditCtrl](../vs140/CRichEditCtrl-Class.md)) to format characters and to retrieve formatting information. For characters, you can specify typeface, size, color, and effects such as bold, italic, and protected.  
  
 You can apply character formatting by using the [SetSelectionCharFormat](../vs140/CRichEditCtrl--SetSelectionCharFormat.md) and [SetWordCharFormat](../vs140/CRichEditCtrl--SetWordCharFormat.md) member functions. To determine the current character formatting for the selected text, use the [GetSelectionCharFormat](../vs140/CRichEditCtrl--GetSelectionCharFormat.md) member function. The [CHARFORMAT](http://msdn.microsoft.com/library/windows/desktop/bb787881) structure is used with these member functions to specify character attributes. One of the important members of **CHARFORMAT** is **dwMask**. In `SetSelectionCharFormat` and `SetWordCharFormat`, **dwMask** specifies which character attributes will be set by this function call. `GetSelectionCharFormat` reports the attributes of the first character in the selection; **dwMask** specifies the attributes that are consistent throughout the selection.  
  
 You can also get and set the "default character formatting," which is the formatting applied to any subsequently inserted characters. For example, if an application sets the default character formatting to bold and the user then types a character, that character is bold. To get and set default character formatting, use the [GetDefaultCharFormat](../vs140/CRichEditCtrl--GetDefaultCharFormat.md) and [SetDefaultCharFormat](../vs140/CRichEditCtrl--SetDefaultCharFormat.md) member functions.  
  
 The "protected" character attribute does not change the appearance of text. If the user attempts to modify protected text, a rich edit control sends its parent window an **EN_PROTECTED** notification message, allowing the parent window to allow or prevent the change. To receive this notification message, you must enable it by using the [SetEventMask](../vs140/CRichEditCtrl--SetEventMask.md) member function. For more information about the event mask, see [Notifications from a Rich Edit Control](../vs140/Notifications-from-a-Rich-Edit-Control.md), later in this topic.  
  
 Foreground color is a character attribute, but background color is a property of the rich edit control. To set the background color, use the [SetBackgroundColor](../vs140/CRichEditCtrl--SetBackgroundColor.md) member function.  
  
## See Also  
 [Using CRichEditCtrl](../vs140/Using-CRichEditCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)