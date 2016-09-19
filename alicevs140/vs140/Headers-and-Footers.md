---
title: "Headers and Footers"
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
ms.assetid: b0be9c53-5773-4955-a777-3c15da745128
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Headers and Footers
This article explains how to add headers and footers to a printed document.  
  
 When you look at a document on the screen, the name of the document and your current location in the document are commonly displayed in a title bar and a status bar. When looking at a printed copy of a document, it's useful to have the name and page number shown in a header or footer. This is a common way in which even WYSIWYG programs differ in how they perform printing and screen display.  
  
 The [OnPrint](../vs140/CView--OnPrint.md) member function is the appropriate place to print headers or footers because it is called for each page, and because it is called only for printing, not for screen display. You can define a separate function to print a header or footer, and pass it the printer device context from `OnPrint`. You might need to adjust the window origin or extent before calling [OnDraw](../vs140/CView--OnDraw.md) to avoid having the body of the page overlap the header or footer. You might also have to modify `OnDraw` because the amount of the document that fits on the page could be reduced.  
  
 One way to compensate for the area taken by the header or footer is to use the **m_rectDraw** member of [CPrintInfo](../vs140/CPrintInfo-Structure.md). Each time a page is printed, this member is initialized with the usable area of the page. If you print a header or footer before printing the body of the page, you can reduce the size of the rectangle stored in **m_rectDraw** to account for the area taken by the header or footer. Then `OnPrint` can refer to **m_rectDraw** to find out how much area remains for printing the body of the page.  
  
 You cannot print a header, or anything else, from [OnPrepareDC](../vs140/CView--OnPrepareDC.md), because it is called before the `StartPage` member function of [CDC](../vs140/CDC-Class.md) has been called. At that point, the printer device context is considered to be at a page boundary. You can perform printing only from the `OnPrint` member function.  
  
## What do you want to know more about?  
  
-   [Printing multipage documents](../vs140/Multipage-Documents.md)  
  
-   [Allocating GDI resources for printing](../vs140/Allocating-GDI-Resources.md)  
  
## See Also  
 [Printing](../vs140/Printing.md)