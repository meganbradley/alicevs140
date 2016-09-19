---
title: "CHeaderCtrl::ClearAllFilters"
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
ms.assetid: a96425fb-62e7-408d-bfbe-1b7bec75cc42
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::ClearAllFilters
Clears all filters for a header control.  
  
## Syntax  
  
```  
BOOL ClearAllFilters();  
```  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method implements the behavior of the Win32 message [HDM_CLEARFILTER](http://msdn.microsoft.com/library/windows/desktop/bb775306) with a column value of –1, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#2)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::ClearFilter](../vs140/CHeaderCtrl--ClearFilter.md)   
 [CHeaderCtrl::EditFilter](../vs140/CHeaderCtrl--EditFilter.md)   
 [CHeaderCtrl::SetFilterChangeTimeout](../vs140/CHeaderCtrl--SetFilterChangeTimeout.md)