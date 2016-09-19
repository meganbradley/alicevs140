---
title: "CSnapInItemImpl::UpdateToolbarButton"
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
ms.assetid: 8453f3bc-5c05-4e83-97be-4e9145083d90
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInItemImpl::UpdateToolbarButton
Call this function to modify a toolbar button, of the snap-in object, before it is displayed.  
  
## Syntax  
  
```  
  
      BOOL UpdateToolbarButton(  
   UINT id,  
   BYTE fsState   
);  
```  
  
#### Parameters  
 `id`  
 Specifies the button ID of the toolbar button to be updated.  
  
 `fsState`  
 Specifies a toolbar button state. If this state is to be set, return **TRUE**. This can be a combination of the following flags:  
  
-   **ENABLED** The button accepts user input. A button that does not have this state does not accept user input and is grayed.  
  
-   **CHECKED** The button has the **CHECKED** style and is being pressed.  
  
-   **HIDDEN** The button is not visible and cannot receive user input.  
  
-   **INDETERMINATE** The button is grayed.  
  
-   **BUTTONPRESSED** The button is being pressed.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInItemImpl Class](../Topic/CSnapInItemImpl%20Class.md)