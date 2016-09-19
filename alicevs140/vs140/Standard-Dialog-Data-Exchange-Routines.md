---
title: "Standard Dialog Data Exchange Routines"
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
ms.assetid: c6adb7f3-f9af-4cc5-a9ea-315c5b60ad1a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Standard Dialog Data Exchange Routines
This topic lists the standard dialog data exchange (DDX) routines used for common MFC dialog controls.  
  
> [!NOTE]
>  The standard dialog data exchange routines are defined in the header file afxdd_.h. However, applications should include afxwin.h.  
  
### DDX Functions  
  
|||  
|-|-|  
|[DDX_CBIndex](../vs140/DDX_CBIndex.md)|Initializes or retrieves the index of the current selection of a combo box control.|  
|[DDX_CBString](../vs140/DDX_CBString.md)|Initializes or retrieves the current contents of the edit field of a combo box control.|  
|[DDX_CBStringExact](../vs140/DDX_CBStringExact.md)|Initializes or retrieves the current contents of the edit field of a combo box control.|  
|[DDX_Check](../vs140/DDX_Check.md)|Initializes or retrieves the current state of a check box control.|  
|[DDX_Control](../vs140/DDX_Control.md)|Subclasses a given control within a dialog box.|  
|[DDX_DateTimeCtrl](../vs140/DDX_DateTimeCtrl.md)|Initializes or retrieves date and/or time data of a date and time picker control.|  
|[DDX_IPAddress](../vs140/DDX_IPAddress.md)|Initializes or retrieves the current value of an IP address control.|  
|[DDX_LBIndex](../vs140/DDX_LBIndex.md)|Initializes or retrieves the index of the current selection of a list box control.|  
|[DDX_LBString](../vs140/DDX_LBString.md)|Initializes or retrieves the current selection within a list box control.|  
|[DDX_LBStringExact](../vs140/DDX_LBStringExact.md)|Initializes or retrieves the current selection within a list box control.|  
|[DDX_MonthCalCtrl](../vs140/DDX_MonthCalCtrl.md)|Initializes or retrieves the current value of a month calendar control.|  
|[DDX_Radio](../vs140/DDX_Radio.md)|Initializes or retrieves the 0-based index of the radio control that is currently checked within a radio control group.|  
|[DDX_Scroll](../vs140/DDX_Scroll.md)|Initializes or retrieves the current position of a scroll control's thumb.|  
|[DDX_Slider](../vs140/DDX_Slider.md)|Initializes or retrieves the current position of a slider control's thumb.|  
|[DDX_Text](../vs140/DDX_Text.md)|Initializes or retrieves the current value of an edit control.|  
  
## See Also  
 [Standard Dialog Data Validation Routines](../vs140/Standard-Dialog-Data-Validation-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)