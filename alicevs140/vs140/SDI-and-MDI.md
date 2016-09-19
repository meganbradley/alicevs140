---
title: "SDI and MDI"
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
ms.assetid: bb7239d9-4759-4f63-bfff-44a04b48c067
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SDI and MDI
MFC makes it easy to work with both single-document interface (SDI) and multiple-document interface (MDI) applications.  
  
 SDI applications allow only one open document frame window at a time. MDI applications allow multiple document frame windows to be open in the same instance of an application. An MDI application has a window within which multiple MDI child windows, which are frame windows themselves, can be opened, each containing a separate document. In some applications, the child windows can be of different types, such as chart windows and spreadsheet windows. In that case, the menu bar can change as MDI child windows of different types are activated.  
  
> [!NOTE]
>  Under Windows 95 and later, applications are commonly SDI because the operating system has adopted a "document-centered" view.  
  
 For more information, see [Documents, Views, and the Framework](../vs140/Documents--Views--and-the-Framework.md).  
  
## See Also  
 [Using the Classes to Write Applications for Windows](../vs140/Using-the-Classes-to-Write-Applications-for-Windows.md)