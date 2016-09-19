---
title: "CWnd::OnVKeyToItem"
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
ms.assetid: 775623bb-394b-4384-b186-76a775364712
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnVKeyToItem
If the `CWnd` object owns a list box with the [LBS_WANTKEYBOARDINPUT](../vs140/List-Box-Styles.md) style, the list box will send the `WM_VKEYTOITEM` message in response to a `WM_KEYDOWN` message.  
  
## Syntax  
  
```  
  
      afx_msg int OnVKeyToItem(   
   UINT nKey,   
   CListBox* pListBox,   
   UINT nIndex    
);  
```  
  
#### Parameters  
 `nKey`  
 Specifies the virtual key code of the key that the user pressed. For a list of of standard virtual key codes, see Winuser.h  
  
 `pListBox`  
 Specifies a pointer to the list box. The pointer may be temporary and should not be stored for later use.  
  
 `nIndex`  
 Specifies the current caret position.  
  
## Return Value  
 Specifies the action that the application performed in response to the message. A return value of –2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box. A return value of –1 indicates that the list box should perform the default action in response to the keystroke. A return value of 0 or greater specifies the zero-based index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the given item.  
  
## Remarks  
 This member function is called by the framework only for list boxes that have the [LBS_HASSTRINGS](../vs140/List-Box-Styles.md) style.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnKeyDown](../vs140/CWnd--OnKeyDown.md)   
 [WM_VKEYTOITEM](http://msdn.microsoft.com/library/windows/desktop/bb761364)