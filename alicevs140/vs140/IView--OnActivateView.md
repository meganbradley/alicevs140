---
title: "IView::OnActivateView"
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
ms.assetid: 7855222d-cbba-489a-ab11-56b4dc99a859
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IView::OnActivateView
Called by MFC when a view is activated or deactivated.  
  
## Syntax  
  
```  
void OnActivateView(  
   bool activate  
);  
```  
  
#### Parameters  
 `activate`  
 Indicates whether the view is being activated or deactivated.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [IView Interface](../vs140/IView-Interface.md)   
 [CView::OnActivateView](../vs140/CView--OnActivateView.md)   
 [How To: Add Command Routing to the Windows Forms Control](../vs140/How-to--Add-Command-Routing-to-the-Windows-Forms-Control.md)