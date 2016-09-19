---
title: "Deriving Controls from a Standard Control"
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
ms.assetid: a6f84315-7007-4e0e-8576-78be81254802
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Deriving Controls from a Standard Control
As with any [CWnd](../vs140/CWnd-Class.md)-derived class, you can modify a control's behavior by deriving a new class from an existing control class.  
  
### To create a derived control class  
  
1.  Derive your class from an existing control class and optionally override the **Create** member function so that it provides the necessary arguments to the base-class **Create** function.  
  
2.  Provide message-handler member functions and message-map entries to modify the control's behavior in response to specific Windows messages. See [Mapping Messages to Functions](../vs140/Mapping-Messages-to-Functions.md).  
  
3.  Provide new member functions to extend the functionality of the control (optional).  
  
 Using a derived control in a dialog box requires extra work. The types and positions of controls in a dialog box are normally specified in a dialog-template resource. If you create a derived control class, you cannot specify it in a dialog template since the resource compiler knows nothing about your derived class.  
  
#### To place your derived control in a dialog box  
  
1.  Embed an object of the derived control class in the declaration of your derived dialog class.  
  
2.  Override the `OnInitDialog` member function in your dialog class to call the `SubclassDlgItem` member function for the derived control.  
  
 `SubclassDlgItem` "dynamically subclasses" a control created from a dialog template. When a control is dynamically subclassed, you hook into Windows, process some messages within your own application, then pass the remaining messages on to Windows. For more information, see the [SubclassDlgItem](../vs140/CWnd--SubclassDlgItem.md) member function of class `CWnd` in the *MFC Reference*. The following example shows how you might write an override of `OnInitDialog` to call `SubclassDlgItem`:  
  
 [!CODE [NVC_MFCControlLadenDialog#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#3)]  
  
 Because the derived control is embedded in the dialog class, it will be constructed when the dialog box is constructed, and it will be destroyed when the dialog box is destroyed. Compare this code to the example in [Adding Controls By Hand](../vs140/Adding-Controls-By-Hand.md).  
  
## See Also  
 [Making and Using Controls](../vs140/Making-and-Using-Controls.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)