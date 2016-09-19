---
title: "CMFCBaseTabCtrl::IsInPlaceEdit"
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
ms.assetid: efbda317-6fd8-43e6-9eaa-a27e0ab6a75e
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCBaseTabCtrl::IsInPlaceEdit
Indicates whether the tab control is configured to enable the user to dynamically modify the tab labels.  
  
## Syntax  
  
```  
virtual BOOL IsInPlaceEdit() const;  
```  
  
## Return Value  
 Nonzero if in-place editing is enabled; otherwise 0.  
  
## Remarks  
 You can enable or disable in-place editing by calling the method [CMFCBaseTabCtrl::EnableInPlaceEdit](../vs140/CMFCBaseTabCtrl--EnableInPlaceEdit.md).  
  
## Requirements  
 **Header:** afxbasetabctrl.h  
  
## See Also  
 [CMFCBaseTabCtrl Class](../vs140/CMFCBaseTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCBaseTabCtrl::EnableInPlaceEdit](../vs140/CMFCBaseTabCtrl--EnableInPlaceEdit.md)