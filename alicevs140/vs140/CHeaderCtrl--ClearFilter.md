---
title: "CHeaderCtrl::ClearFilter"
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
ms.assetid: 605366ca-f24f-49e9-b981-6ca39f70da7b
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::ClearFilter
Clears the filter for a header control.  
  
## Syntax  
  
```  
BOOL ClearFilter(  
   int nColumn  
);  
```  
  
#### Parameters  
 `nColumn`  
 Column value indicating which filter to clear.  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method implements the behavior of the Win32 message [HDM_CLEARFILTER](http://msdn.microsoft.com/library/windows/desktop/bb775306), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#3)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::ClearAllFilters](../vs140/CHeaderCtrl--ClearAllFilters.md)   
 [CHeaderCtrl::EditFilter](../vs140/CHeaderCtrl--EditFilter.md)   
 [CHeaderCtrl::SetFilterChangeTimeout](../vs140/CHeaderCtrl--SetFilterChangeTimeout.md)