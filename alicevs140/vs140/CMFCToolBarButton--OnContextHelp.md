---
title: "CMFCToolBarButton::OnContextHelp"
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
ms.assetid: 55fe8b92-98a3-4bc5-a826-ddb094ce2ea8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::OnContextHelp
Called by the framework when the parent toolbar handles a `WM_HELPHITTEST` message.  
  
## Syntax  
  
```  
virtual BOOL OnContextHelp(  
   CWnd* pWnd  
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 The parent window of the toolbar button.  
  
## Return Value  
 This method returns `FALSE`.  
  
## Remarks  
 The default implementation of this method does nothing and returns `FALSE`. Override this method to return a nonzero value if the button processes the help message.  
  
 For more information about the `WM_HELPHITTEST` message, see [TN028: Context-Sensitive Help Support](../vs140/TN028--Context-Sensitive-Help-Support.md).  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TN028: Context-Sensitive Help Support](../vs140/TN028--Context-Sensitive-Help-Support.md)