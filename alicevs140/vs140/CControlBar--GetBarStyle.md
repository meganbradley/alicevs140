---
title: "CControlBar::GetBarStyle"
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
ms.assetid: dcc6494c-32cc-46b4-913b-48480c89f45b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::GetBarStyle
Call this function to determine which **CBRS_** (control bar styles) settings are currently set for the control bar.  
  
## Syntax  
  
```  
  
DWORD GetBarStyle( );  
```  
  
## Return Value  
 The current **CBRS_** (control bar styles) settings for the control bar. See [CControlBar::SetBarStyle](../vs140/CControlBar--SetBarStyle.md) for the complete list of available styles.  
  
## Remarks  
 Does not handle **WS_** (window style) styles.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CControlBar::SetBarStyle](../vs140/CControlBar--SetBarStyle.md)