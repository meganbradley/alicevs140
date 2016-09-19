---
title: "CDateTimeCtrl::GetMonthCalColor"
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
ms.assetid: 3ef42768-2400-4e9b-bd58-141be6c3821c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::GetMonthCalColor
Retrieves the color for a given portion of the month calendar within the date and time picker control.  
  
## Syntax  
  
```  
  
      COLORREF GetMonthCalColor(  
   int iColor   
) const;  
```  
  
#### Parameters  
 `iColor`  
 An `int` value specifying which color area of the month calendar to retrieve. For a list of values, see the `iColor` parameter for [SetMonthCalColor](../vs140/CDateTimeCtrl--SetMonthCalColor.md).  
  
## Return Value  
 A **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful. The function returns -1 if unsuccessful.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [DTM_GETMCCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb761759), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CDateTimeCtrl#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl#2)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDateTimeCtrl::SetMonthCalColor](../vs140/CDateTimeCtrl--SetMonthCalColor.md)