---
title: "CDateTimeCtrl::GetMonthCalCtrl"
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
ms.assetid: 80db45df-e256-421e-b2b7-a8c984154c40
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::GetMonthCalCtrl
Retrieves the `CMonthCalCtrl` object associated with the date and time picker control.  
  
## Syntax  
  
```  
  
CMonthCalCtrl* GetMonthCalCtrl( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CMonthCalCtrl](../vs140/CMonthCalCtrl-Class.md) object, or **NULL** if unsuccessful or if the window is not visible.  
  
## Remarks  
 Date and time picker controls create a child month calendar control when the user clicks the drop-down arrow. When the `CMonthCalCtrl` object is no longer needed, it is destroyed, so your application must not rely on storing the object representing the date time picker control's child month calendar.  
  
## Example  
 [!CODE [NVC_MFC_CDateTimeCtrl#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl#3)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)