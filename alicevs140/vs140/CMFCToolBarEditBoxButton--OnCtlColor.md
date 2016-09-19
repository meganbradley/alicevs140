---
title: "CMFCToolBarEditBoxButton::OnCtlColor"
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
ms.assetid: 1486c128-f22c-4b1b-8008-24cc2217f3b8
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::OnCtlColor
Called by the framework when the parent toolbar handles a `WM_CTLCOLOR` message.  
  
## Syntax  
  
```  
virtual HBRUSH OnCtlColor(  
   CDC* pDC,  
   UINT nCtlColor  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 The device context that displays the button.  
  
 [in] `nCtlColor`  
 Unused.  
  
## Return Value  
 A handle to the global window brush.  
  
## Remarks  
 This method overrides the base class implementation ([CMFCToolBarButton::OnCtlColor](../vs140/CMFCToolBarButton--OnCtlColor.md)) by setting the text and background colors of the provided device context to the global text and background colors, respectively.  
  
 For more information about global options that are available to your application, see [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md).  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnCtlColor](../vs140/CMFCToolBarButton--OnCtlColor.md)   
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)