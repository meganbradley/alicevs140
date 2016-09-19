---
title: "CMFCToolBar::IsExistCustomizeButton"
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
ms.assetid: 9f518b89-e03d-4bc7-bea5-29a484c1a4fc
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::IsExistCustomizeButton
Determines whether the toolbar contains the **Customize** button.  
  
## Syntax  
  
```  
BOOL IsExistCustomizeButton();  
```  
  
## Return Value  
 `TRUE` if the toolbar contains the **Customize** button; otherwise `FALSE`.  
  
## Remarks  
 If this method returns `TRUE`, the [CMFCToolBar::GetCustomizeButton](../vs140/CMFCToolBar--GetCustomizeButton.md) method returns a pointer to the **Customize** button that appears at the end of the toolbar.  
  
 Use the [CMFCToolBar::EnableCustomizeButton](../vs140/CMFCToolBar--EnableCustomizeButton.md) method to add the **Customize** button to your toolbar.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCCustomizeButton Class](assetId:///f0a1da67-dcd4-4f40-bc1d-a8ee4184c647)   
 [CMFCToolBar::GetCustomizeButton](../vs140/CMFCToolBar--GetCustomizeButton.md)   
 [CMFCToolBar::EnableCustomizeButton](../vs140/CMFCToolBar--EnableCustomizeButton.md)