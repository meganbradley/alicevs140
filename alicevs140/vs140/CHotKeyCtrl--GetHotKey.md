---
title: "CHotKeyCtrl::GetHotKey"
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
ms.assetid: e8ce71d6-18fc-4ba1-b62b-2e84e1c6944c
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHotKeyCtrl::GetHotKey
Retrieves the virtual key code and modifier flags of a keyboard shortcut from a hot key control.  
  
## Syntax  
  
```  
DWORD GetHotKey() const;  
void GetHotKey(  
   WORD &wVirtualKeyCode,  
   WORD &wModifiers  
) const;  
```  
  
#### Parameters  
 [out] `wVirtualKeyCode`  
 Virtual key code of the keyboard shortcut. For a list of standard virtual key codes, see Winuser.h.  
  
 [out] `wModifiers`  
 A bitwise combination (OR) of flags that indicate the modifier keys in the keyboard shortcut.  
  
 The modifier flags are as follows:  
  
|Flag|Corresponding Key|  
|----------|-----------------------|  
|`HOTKEYF_ALT`|ALT key|  
|`HOTKEYF_CONTROL`|CTRL key|  
|`HOTKEYF_EXT`|Extended key|  
|`HOTKEYF_SHIFT`|SHIFT key|  
  
## Return Value  
 In the first overloaded method, a `DWORD` that contains the virtual key code and modifier flags. The low-order byte of the low-order word contains the virtual key code, the high-order byte of the low-order word contains the modifier flags, and the high-order word is zero.  
  
## Remarks  
 The virtual key code and the modifier keys together define the keyboard shortcut.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHotKeyCtrl Class](../vs140/CHotKeyCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHotKeyCtrl::SetHotKey](../vs140/CHotKeyCtrl--SetHotKey.md)