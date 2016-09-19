---
title: "CMonthCalCtrl::GetMaxTodayWidth"
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
ms.assetid: b29f654d-a5d8-489f-ba42-f746eb1331a5
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetMaxTodayWidth
Retrieves the maximum width of the "Today" string for the current month calendar control.  
  
## Syntax  
  
```  
DWORD GetMaxTodayWidth() const;  
```  
  
## Return Value  
 The width of the "Today" string, in pixels.  
  
## Example  
 The following code example defines the variable, `m_monthCalCtrl`, that is used to programmatically access the month calendar control. This variable is used in the next example.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#9)]  
  
## Example  
 The following code example demonstrates the `GetMaxTodayWidth` method.  
  
 [!CODE [NVC_MFC_CMonthCalCtrl_s1#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl_s1#1)]  
  
## Remarks  
 The user can return to the current date by clicking the "Today" string, which is displayed at the bottom of the month calendar control. The "Today" string includes label text and date text.  
  
 This method sends the [MCM_GETMAXTODAYWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb760962) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MCM_GETMAXTODAYWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb760962)