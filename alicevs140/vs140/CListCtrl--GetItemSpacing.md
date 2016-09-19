---
title: "CListCtrl::GetItemSpacing"
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
ms.assetid: 5bd9e509-f188-4c0b-9e1f-6b1e6183a2c7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetItemSpacing
Calculates the spacing between items in the current list-view control.  
  
## Syntax  
  
```  
BOOL GetItemSpacing(  
     BOOL fSmall,   
     int* pnHorzSpacing,   
     int* pnVertSpacing  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `fSmall`|View for which to retrieve the item spacing. Specify `true` for small icon view, or `false` for icon view.|  
|[out] `pnHorzSpacing`|Contains the horizontal spacing between items.|  
|[out] `pnVertSpacing`|Contains the vertical spacing between items.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [LVM_GETITEMSPACING](http://msdn.microsoft.com/library/windows/desktop/bb761051) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in Windows NT 3.51 and later.  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LVM_GETITEMSPACING](http://msdn.microsoft.com/library/windows/desktop/bb761051)