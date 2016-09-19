---
title: "CHotKeyCtrl::GetKeyName"
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
ms.assetid: 0ba2503c-d893-4a92-9711-5e760aad0dc2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHotKeyCtrl::GetKeyName
Call this member function to get the localized name of the key assigned to a specified virtual key code.  
  
## Syntax  
  
```  
  
      static CString GetKeyName(  
   UINT vk,  
   BOOL fExtended   
);  
```  
  
#### Parameters  
 `vk`  
 The virtual key code.  
  
 *fExtended*  
 If the virtual key code is an extended key, **TRUE**; otherwise **FALSE**.  
  
## Return Value  
 The localized name of the key specified by the `vk` parameter. If the key has no mapped name, `GetKeyName` returns an empty string.  
  
## Remarks  
 The key name that this function returns comes from the keyboard driver, so you can install a non-localized keyboard driver in a localized version of Windows, and vice versa.  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#69](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#69)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHotKeyCtrl Class](../vs140/CHotKeyCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_KEYDOWN](http://msdn.microsoft.com/library/windows/desktop/ms646280)   
 [GetKeyNameText](http://msdn.microsoft.com/library/windows/desktop/ms646300)   
 [CHotKeyCtrl::GetHotKeyName](../vs140/CHotKeyCtrl--GetHotKeyName.md)