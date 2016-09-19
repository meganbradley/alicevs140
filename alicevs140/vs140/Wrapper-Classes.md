---
title: "Wrapper Classes"
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
ms.assetid: ebbc17b9-cc1b-4c29-afa9-da7f9511876e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Wrapper Classes
When you [insert a control](../vs140/Inserting-the-Control-into-a-Visual-C---Application.md) into a Visual C++ project, wrapper classes for the control are not included by default. However, if you want to [modify the control's behavior](../vs140/Modifying-a-Control-s-Run-Time-Behavior.md), you can write a wrapper class for the control. Depending on how you intend to manipulate the control programmatically, you need to write one or more of the control's wrapper classes.  
  
 A wrapper class is available for each of the coclasses in the control's type library (.tlb) file. The control's wrapper class should be the control name prefixed by the letter C.  
  
 For more information about the functionality of the wrapper classes, see the object model for the control's base technology.  
  
 Using [CWnd::GetDlgItem](../vs140/CWnd--GetDlgItem.md) also requires wrapper classes because the return value must be cast to the control class. For example:  
  
```  
CDBList* pDBList = 0;  
pDBList = static_cast<CDBList*>(GetDlgItem(IDC_DBLIST));  
```  
  
 By reading the generated .idl file, you can determine what properties, methods, and events are exposed by a control, as well as see method and accessor function declarations directly. Additional information can be obtained from the control using the [OLE/COM Object Viewer](../vs140/Using-the-OLE-COM-Object-Viewer.md).  
  
## See Also  
 [Using ActiveX Controls](../vs140/Using-ActiveX-Controls.md)   
 [Modifying a Control's Run-Time Behavior](../vs140/Modifying-a-Control-s-Run-Time-Behavior.md)