---
title: "CMFCToolBarDateTimeCtrl::CMFCToolBarDateTimeCtrl"
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
ms.topic: reference
ms.assetid: 5ed2abbe-7d42-45fc-bd73-fcf1129eaf4d
caps.latest.revision: 21
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::CMFCToolBarDateTimeCtrl
Creates and initializes a [CMFCToolBarDateTimeCtrl](../vs140/CMFCToolBarDateTimeCtrl-Class.md) object.  
  
## Syntax  
  
```  
CMFCToolBarDateTimeCtrl(  
   UINT uiID,  
   int iImage,  
   DWORD dwStyle=0,  
   int iWidth=0  
);  
```  
  
#### Parameters  
 [in] `uiID`  
 The control ID.  
  
 [in] `iImage`  
 The index of the image in the toolbar's `CMFCToolBarImages` object.  
  
 [in] `dwStyle`  
 The style of the `CMFCToolBarDateTimeCtrlImpl` window that is created when a user clicks the button.  
  
 [in] `iWidth`  
 The width of the control, in pixels.  
  
## Remarks  
 This object is initialized to the system date and time. The window style of the internal `CMFCToolBarDateTimeCtrlImpl` object includes the `dwStyle` parameter and the `WS_CHILD` and `WS_VISIBLE` styles. You cannot change these styles by using `CMFCToolBarDateTimeCtrl::SetStyle`. Use `SetStyle` to change the style of the `CMFCToolBarDateTimeCtrl` control.  
  
## Example  
 The following example demonstrates how to construct an object of the `CMFCToolBarDateTimeCtrl` class. This code snippet is part of the [Toolbar Date Time Picker sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_ToolbarDateTimePicker#1](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_ToolbarDateTimePicker#1)]  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [CMFCToolBarDateTimeCtrlImpl Class](assetId:///4fcddcbc-b374-4c27-bfb4-09fb0ca2eac5)