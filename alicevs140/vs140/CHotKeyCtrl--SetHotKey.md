---
title: "CHotKeyCtrl::SetHotKey"
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
ms.assetid: 5d719775-be11-4e58-be87-a8522120aa4b
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHotKeyCtrl::SetHotKey
Sets the keyboard shortcut for a hot key control.  
  
## Syntax  
  
```  
void SetHotKey(  
   WORD wVirtualKeyCode,  
   WORD wModifiers  
);  
```  
  
#### Parameters  
 [in] `wVirtualKeyCode`  
 Virtual key code of the keyboard shortcut. For a list of standard virtual key codes, see Winuser.h.  
  
 [in] `wModifiers`  
 A bitwise combination (OR) of flags that indicate the modifier keys in the keyboard shortcut.  
  
 The modifier flags are as follows:  
  
|Flag|Corresponding Key|  
|----------|-----------------------|  
|`HOTKEYF_ALT`|ALT key|  
|`HOTKEYF_CONTROL`|CTRL key|  
|`HOTKEYF_EXT`|Extended key|  
|`HOTKEYF_SHIFT`|SHIFT key|  
  
## Remarks  
 The virtual key code and the modifier keys together define the keyboard shortcut.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHotKeyCtrl Class](../vs140/CHotKeyCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHotKeyCtrl::GetHotKey](../vs140/CHotKeyCtrl--GetHotKey.md)