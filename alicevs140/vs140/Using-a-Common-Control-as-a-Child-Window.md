---
title: "Using a Common Control as a Child Window"
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
ms.assetid: 608f7d47-7854-4fce-bde9-856c51e76753
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using a Common Control as a Child Window
Any of the Windows common controls can be used as a child window of any other window. The following procedure describes how to create a common control dynamically and then work with it.  
  
### To use a common control as a child window  
  
1.  Define the control in the related class or handler.  
  
2.  Use the control's override of the [CWnd::Create](../vs140/CWnd--Create.md) method to create the Windows control.  
  
3.  After the control has been created (as early as the `OnCreate` handler if you subclass the control), you can manipulate the control using its member functions. See the descriptions of individual controls at [Controls (MFC)](../vs140/Controls--MFC-.md) for details on methods.  
  
4.  When you are finished with the control, use [CWnd::DestroyWindow](../vs140/CWnd--DestroyWindow.md) to destroy the control.  
  
## See Also  
 [Making and Using Controls](../vs140/Making-and-Using-Controls.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)