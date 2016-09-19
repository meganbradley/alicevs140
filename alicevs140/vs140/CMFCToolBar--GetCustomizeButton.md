---
title: "CMFCToolBar::GetCustomizeButton"
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
ms.assetid: 1c37d1a4-90dd-41a8-85f8-b1f272e2d9b4
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetCustomizeButton
Retrieves a pointer to the `CMFCCustomizeButton` object that is associated with the toolbar.  
  
## Syntax  
  
```  
CMFCCustomizeButton* GetCustomizeButton();  
```  
  
## Return Value  
 A pointer to the `CMFCCustomizeButton` object that is associated with the toolbar.  
  
## Remarks  
 This method retrieves the **Customize** button that appears at the end of the toolbar. Use the [CMFCToolBar::EnableCustomizeButton](../vs140/CMFCToolBar--EnableCustomizeButton.md) method to add the **Customize** button to your toolbar.  
  
 You can call the [CMFCToolBar::IsExistCustomizeButton](../vs140/CMFCToolBar--IsExistCustomizeButton.md) method to determine whether the toolbar contains a valid `CMFCCustomizeButton` object.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCCustomizeButton Class](assetId:///f0a1da67-dcd4-4f40-bc1d-a8ee4184c647)   
 [CMFCToolBar::EnableCustomizeButton](../vs140/CMFCToolBar--EnableCustomizeButton.md)   
 [CMFCToolBar::IsExistCustomizeButton](../vs140/CMFCToolBar--IsExistCustomizeButton.md)