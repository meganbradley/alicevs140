---
title: "CMFCToolBarEditBoxButton::GetContentsAll"
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
ms.assetid: ede51e57-cd7d-41fc-b34c-d0b684ca7f94
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::GetContentsAll
Retrieves the text of the first edit box toolbar control that has the specified command ID.  
  
## Syntax  
  
```  
static CString __stdcall GetContentsAll(  
   UINT uiCmd  
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The command ID of the button from which to retrieve contents.  
  
## Return Value  
 A `CString` object that contains the text of the first edit box toolbar control that has the specified command ID.  
  
## Remarks  
 This method returns the empty string if no `CMFCToolBarEditBoxButton` objects have the specified command ID.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)