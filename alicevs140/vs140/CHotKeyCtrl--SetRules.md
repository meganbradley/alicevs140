---
title: "CHotKeyCtrl::SetRules"
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
ms.assetid: 26f5be4e-b3be-4f5c-b384-8fe567984876
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHotKeyCtrl::SetRules
Call this function to define the invalid combinations and the default modifier combination for a hot key control.  
  
## Syntax  
  
```  
  
      void SetRules(  
   WORD wInvalidComb,  
   WORD wModifiers   
);  
```  
  
#### Parameters  
 `wInvalidComb`  
 Array of flags that specifies invalid key combinations. It can be a combination of the following values:  
  
-   `HKCOMB_A` ALT  
  
-   `HKCOMB_C` CTRL  
  
-   `HKCOMB_CA` CTRL+ALT  
  
-   `HKCOMB_NONE` Unmodified keys  
  
-   `HKCOMB_S` SHIFT  
  
-   `HKCOMB_SA` SHIFT+ALT  
  
-   `HKCOMB_SC` SHIFT+CTRL  
  
-   `HKCOMB_SCA` SHIFT+CTRL+ALT  
  
 `wModifiers`  
 Array of flags that specifies the key combination to use when the user enters an invalid combination. For more information on the modifier flags, see [GetHotKey](../vs140/CHotKeyCtrl--GetHotKey.md).  
  
## Remarks  
 When a user enters an invalid key combination, as defined by flags specified in `wInvalidComb`, the system uses the OR operator to combine the keys entered by the user with the flags specified in `wModifiers`. The resulting key combination is converted into a string and then displayed in the hot key control.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHotKeyCtrl Class](../vs140/CHotKeyCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHotKeyCtrl::GetHotKey](../vs140/CHotKeyCtrl--GetHotKey.md)   
 [CHotKeyCtrl::SetHotKey](../vs140/CHotKeyCtrl--SetHotKey.md)