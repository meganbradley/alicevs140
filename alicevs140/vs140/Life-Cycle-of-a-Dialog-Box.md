---
title: "Life Cycle of a Dialog Box"
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
ms.assetid: e16fd78e-238d-4f31-8c9d-8564f3953bd9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Life Cycle of a Dialog Box
During the life cycle of a dialog box, the user invokes the dialog box, typically inside a command handler that creates and initializes the dialog object, the user interacts with the dialog box, and the dialog box closes.  
  
 For modal dialog boxes, your handler gathers any data the user entered once the dialog box closes. Since the dialog object exists after its dialog window has closed, you can simply use the member variables of your dialog class to extract the data.  
  
 For modeless dialog boxes, you may often extract data from the dialog object while the dialog box is still visible. At some point, the dialog object is destroyed; when this happens depends on your code.  
  
## What do you want to know more about?  
  
-   [Creating and displaying dialog boxes](../vs140/Creating-and-Displaying-Dialog-Boxes.md)  
  
-   [Creating modal dialog boxes](../vs140/Creating-Modal-Dialog-Boxes.md)  
  
-   [Creating modeless dialog boxes](../vs140/Creating-Modeless-Dialog-Boxes.md)  
  
-   [Using a dialog template in memory](../vs140/Using-a-Dialog-Template-in-Memory.md)  
  
-   [Setting the dialog box's background color](../vs140/Setting-the-Dialog-Box’s-Background-Color.md)  
  
-   [Initializing the dialog box](../vs140/Initializing-the-Dialog-Box.md)  
  
-   [Handling Windows messages in your dialog box](../vs140/Handling-Windows-Messages-in-Your-Dialog-Box.md)  
  
-   [Retrieving data from the dialog object](../vs140/Retrieving-Data-from-the-Dialog-Object.md)  
  
-   [Closing the dialog box](../vs140/Closing-the-Dialog-Box.md)  
  
-   [Destroying the dialog box](../vs140/Destroying-the-Dialog-Box.md)  
  
-   [Dialog data exchange (DDX) and validation (DDV)](../vs140/Dialog-Data-Exchange-and-Validation.md)  
  
-   [Property sheet dialog boxes](../vs140/Property-Sheets-and-Property-Pages--MFC-.md)  
  
## See Also  
 [Dialog Boxes](../vs140/Dialog-Boxes.md)