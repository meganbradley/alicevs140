---
title: "Using Views"
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
ms.assetid: dc3de6ad-5c64-4317-8f10-8bdcc38cdbd5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Views
The view's responsibilities are to display the document's data graphically to the user and to accept and interpret user input as operations on the document. Your tasks in writing your view class are to:  
  
-   Write your view class's [OnDraw](../vs140/CView--OnDraw.md) member function, which renders the document's data.  
  
-   Connect appropriate Windows messages and user-interface objects such as menu items to message-handler member functions in the view class.  
  
-   Implement those handlers to interpret user input.  
  
 In addition, you may need to override other `CView` member functions in your derived view class. In particular, you may want to override [OnInitialUpdate](../vs140/CView--OnInitialUpdate.md) to perform special initialization for the view and [OnUpdate](../vs140/CView--OnUpdate.md) to do any special processing needed just before the view redraws itself. For multipage documents, you also must override [OnPreparePrinting](../vs140/CView--OnPreparePrinting.md) to initialize the Print dialog box with the number of pages to print and other information. For more information on overriding `CView` member functions, see class [CView](../vs140/CView-Class.md) in the *MFC Reference*.  
  
## What do you want to know more about?  
  
-   [Derived view classes available in MFC](../vs140/Derived-View-Classes-Available-in-MFC.md)  
  
-   [Drawing in a view](../vs140/Drawing-in-a-View.md)  
  
-   [Interpreting user input through a view](../vs140/Interpreting-User-Input-Through-a-View.md)  
  
-   [The role of the view in printing](../vs140/Role-of-the-View-in-Printing.md)  
  
-   [Scrolling and scaling views](../vs140/Scrolling-and-Scaling-Views.md)  
  
-   [Initializing and cleaning up documents and views](../vs140/Initializing-and-Cleaning-Up-Documents-and-Views.md)  
  
## See Also  
 [Document/View Architecture](../vs140/Document-View-Architecture.md)   
 [CFormView Class](../vs140/CFormView-Class.md)   
 [Record Views  (MFC Data Access)](../vs140/Record-Views---MFC-Data-Access-.md)   
 [Bypassing the Serialization Mechanism](../vs140/Bypassing-the-Serialization-Mechanism.md)