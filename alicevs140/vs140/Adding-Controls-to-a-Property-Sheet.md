---
title: "Adding Controls to a Property Sheet"
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
ms.topic: article
ms.assetid: 24ad4c0b-c1db-4850-b9f0-34aae8d74571
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Adding Controls to a Property Sheet
By default, a property sheet allocates window area for the property pages, the tab index, and the OK, Cancel, and Apply buttons. (A modeless property sheet does not have the OK, Cancel, and Apply buttons.) You can add other controls to the property sheet. For example, you can add a preview window to the right of the property page area to show the user what the current settings would look like if applied to an external object.  
  
 You can add controls to the property sheet dialog in the `OnCreate` handler. Accommodating additional controls usually requires expanding the size of the property sheet dialog. After calling the base class **CPropertySheet::OnCreate**, call [GetWindowRect](../vs140/CWnd--GetWindowRect.md) to get the width and height of the currently allocated property sheet window, expand the rectangle's dimensions, and call [MoveWindow](../vs140/CWnd--MoveWindow.md) to change the size of the property sheet window.  
  
## See Also  
 [Property Sheets](../vs140/Property-Sheets--MFC-.md)   
 [CPropertyPage Class](../vs140/CPropertyPage-Class.md)   
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)