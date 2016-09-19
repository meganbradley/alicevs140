---
title: "Connecting a Pop-up Menu to Your Application"
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
ms.assetid: 295cbf0e-6416-478e-bc3d-472fb98e0e52
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Connecting a Pop-up Menu to Your Application
### To connect a pop-up menu to your application  
  
1.  Add a message handler for [WM_CONTEXTMENU](_win32_WM_CONTEXTMENU) (for example). For more information, see [Mapping Messages to Functions](../vs140/Mapping-Messages-to-Functions.md).  
  
2.  Add the following code to the message handler:  
  
    ```  
    CMenu menu;  
    VERIFY(menu.LoadMenu(IDR_MENU1));  
    CMenu* pPopup = menu.GetSubMenu(0);  
    ASSERT(pPopup != NULL);  
    pPopup->TrackPopupMenu(TPM_LEFTALIGN | TPM_RIGHTBUTTON, point.x, point.y, AfxGetMainWnd());  
    ```  
  
    > [!NOTE]
    >  The [CPoint](../vs140/CPoint-Class.md) **passed by the message handler is in screen coordinates.**  
  
 For information on adding resources to managed projects, please see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see [Walkthrough: Using Resources for Localization with ASP.NET](assetId:///bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
 **Requirements**  
  
 MFC  
  
## See Also  
 [Creating Pop-up Menus](../vs140/Creating-Pop-up-Menus.md)   
 [Menu Editor](../vs140/Menu-Editor.md)   
 [Menus](_win32_Menus)