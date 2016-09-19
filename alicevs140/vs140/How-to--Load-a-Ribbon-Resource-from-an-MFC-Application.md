---
title: "How to: Load a Ribbon Resource from an MFC Application"
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
ms.assetid: 1c76bb8f-6345-414a-9f3f-128815ceadc5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Load a Ribbon Resource from an MFC Application
To use the ribbon resource in your application, modify the application to load the ribbon resource.  
  
### To load a ribbon resource  
  
1.  Declare the `Ribbon Control` object in the `CMainFrame` class.  
  
    ```  
    CMFCRibbonBar m_wndRibbonBar;   
    ```  
  
2.  In `CMainFrame::OnCreate`, create and initialize the Ribbon Control.  
  
    ```  
    if (!m_wndRibbonBar.Create (this))  
    {  
        return -1;  
    }  
  
    if (!m_wndRibbonBar.LoadFromResource(IDR_RIBBON))  
    {  
        return -1;  
    }  
    ```  
  
## See Also  
 [Ribbon Designer (MFC)](../vs140/Ribbon-Designer--MFC-.md)