---
title: "CHeaderCtrl::EditFilter"
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
ms.assetid: b72acba0-9252-4230-a271-378255cf0449
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::EditFilter
Begins to edit the specified filter of a header control.  
  
## Syntax  
  
```  
BOOL EditFilter(  
   int nColumn,  
   BOOL bDiscardChanges  
);  
```  
  
#### Parameters  
 `nColumn`  
 The column to edit.  
  
 `bDiscardChanges`  
 A value that specifies how to handle the user's editing changes if the user is in the process of editing the filter when the [HDM_EDITFILTER](http://msdn.microsoft.com/library/windows/desktop/bb775312) message is sent.  
  
 Specify `true` to discard the changes made by the user, or `false` to accept the changes made by the user.  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method implements the behavior of the Win32 message [HDM_EDITFILTER](http://msdn.microsoft.com/library/windows/desktop/bb775312), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#7)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::ClearAllFilters](../vs140/CHeaderCtrl--ClearAllFilters.md)   
 [CHeaderCtrl::ClearFilter](../vs140/CHeaderCtrl--ClearFilter.md)   
 [CHeaderCtrl::SetFilterChangeTimeout](../vs140/CHeaderCtrl--SetFilterChangeTimeout.md)