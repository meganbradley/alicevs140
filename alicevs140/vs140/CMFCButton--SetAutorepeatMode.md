---
title: "CMFCButton::SetAutorepeatMode"
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
ms.assetid: f591236f-6588-41d9-98f4-d80ad6dee550
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::SetAutorepeatMode
Sets a button to auto-repeat mode.  
  
## Syntax  
  
```  
void SetAutorepeatMode(  
   int nTimeDelay=500   
);  
```  
  
#### Parameters  
 [in] `nTimeDelay`  
 A nonnegative number that specifies the interval between messages that are sent to the parent window. The interval is measured in milliseconds and its default value is 500 milliseconds. Specify zero to disable auto-repeat message mode.  
  
## Remarks  
 This method causes the button to constantly send WM_COMMAND messages to the parent window until the button is released, or the `nTimeDelay` parameter is set to zero.  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)