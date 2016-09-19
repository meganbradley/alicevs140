---
title: "Property Sheets and Property Pages (MFC)"
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
ms.assetid: de8fea12-6c35-4cef-8625-b8073a379446
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property Sheets and Property Pages (MFC)
An MFC [dialog box](../vs140/Dialog-Boxes.md) can take on a "tab dialog" look by incorporating property sheets and property pages. Called a "property sheet" in MFC, this kind of dialog box, similar to many dialog boxes in Microsoft Word, Excel, and Visual C++, appears to contain a stack of tabbed sheets, much like a stack of file folders seen from front to back, or a group of cascaded windows. Controls on the front tab are visible; only the labeled tab is visible on the rear tabs. Property sheets are particularly useful for managing large numbers of properties or settings that fall fairly neatly into several groups. Typically, one property sheet can simplify a user interface by replacing several separate dialog boxes.  
  
 As of MFC version 4.0, property sheets and property pages are implemented using the common controls that come with Windows 95 and Windows NT version 3.51 and later.  
  
 Property sheets are implemented with classes [CPropertySheet](../vs140/CPropertySheet-Class.md) and [CPropertyPage](../vs140/CPropertyPage-Class.md) (described in the *MFC Reference*). `CPropertySheet` defines the overall dialog box, which can contain multiple "pages" based on `CPropertyPage`.  
  
 For information on creating and working with property sheets, see the topic [Property Sheets](../vs140/Property-Sheets--MFC-.md).  
  
## See Also  
 [Dialog Boxes](../vs140/Dialog-Boxes.md)   
 [Life Cycle of a Dialog Box](../vs140/Life-Cycle-of-a-Dialog-Box.md)   
 [Property Sheets and Property Pages in MFC](../vs140/Property-Sheets-and-Property-Pages-in-MFC.md)   
 [Exchanging Data](../vs140/Exchanging-Data.md)   
 [Creating a Modeless Property Sheet](../vs140/Creating-a-Modeless-Property-Sheet.md)   
 [Handling the Apply Button](../vs140/Handling-the-Apply-Button.md)