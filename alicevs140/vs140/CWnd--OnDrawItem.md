---
title: "CWnd::OnDrawItem"
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
ms.assetid: 1dc50277-7b58-41bb-891d-8c592483b5c6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnDrawItem
The framework calls this member function for the owner of an owner-draw button control, combo-box control, list-box control, or menu when a visual aspect of the control or menu has changed.  
  
## Syntax  
  
```  
  
      afx_msg void OnDrawItem(  
   int nIDCtl,  
   LPDRAWITEMSTRUCT lpDrawItemStruct   
);  
```  
  
#### Parameters  
 `nIDCtl`  
 Contains the identifier of the control that sent the `WM_DRAWITEM` message. If a menu sent the message, `nIDCtl` contains 0.  
  
 `lpDrawItemStruct`  
 Specifies a long pointer to a `DRAWITEMSTRUCT` data structure that contains information about the item to be drawn and the type of drawing required.  
  
## Remarks  
 The **itemAction** member of the [DRAWITEMSTRUCT](../vs140/DRAWITEMSTRUCT-Structure.md) structure defines the drawing operation that is to be performed. The data in this member allows the owner of the control to determine what drawing action is required.  
  
 Before returning from processing this message, an application should ensure that the device context identified by the `hDC` member of the `DRAWITEMSTRUCT` structure is restored to the default state.  
  
 If the **hwndItem** member belongs to a [CButton](../vs140/CButton-Class.md), [CMenu](../vs140/CMenu-Class.md), [CListBox](../vs140/CListBox-Class.md), or [CComboBox](../vs140/CComboBox-Class.md) object, then the `DrawItem` virtual function of the appropriate class is called. Override the `DrawItem` member function of the appropriate control's class to draw the item.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DRAWITEMSTRUCT Structure](../vs140/DRAWITEMSTRUCT-Structure.md)   
 [WM_DRAWITEM](http://msdn.microsoft.com/library/windows/desktop/bb775923)   
 [CButton::DrawItem](../vs140/CButton--DrawItem.md)   
 [CMenu::DrawItem](../vs140/CMenu--DrawItem.md)   
 [CListBox::DrawItem](../vs140/CListBox--DrawItem.md)   
 [CComboBox::DrawItem](../vs140/CComboBox--DrawItem.md)