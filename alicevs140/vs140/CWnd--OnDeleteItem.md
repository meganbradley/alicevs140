---
title: "CWnd::OnDeleteItem"
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
ms.assetid: 8d3ca9c7-7496-4520-a35d-0cbcb736251d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnDeleteItem
The framework calls this member function to inform the owner of an owner-draw list box or combo box that the list box or combo box is destroyed or that items have been removed by [CComboBox::DeleteString](../vs140/CComboBox--DeleteString.md), [CListBox::DeleteString](../vs140/CListBox--DeleteString.md), [CComboBox::ResetContent](../vs140/CComboBox--ResetContent.md), or [CListBox::ResetContent](../vs140/CListBox--ResetContent.md).  
  
## Syntax  
  
```  
  
      afx_msg void OnDeleteItem(  
   int nIDCtl,  
   LPDELETEITEMSTRUCT lpDeleteItemStruct   
);  
```  
  
#### Parameters  
 `nIDCtl`  
 The identifier of the control that sent the `WM_DELETEITEM` message.  
  
 `lpDeleteItemStruct`  
 Specifies a long pointer to a [DELETEITEMSTRUCT](../vs140/DELETEITEMSTRUCT-Structure.md) data structure that contains information about the deleted list box item.  
  
## Remarks  
 If the **hwndItem** member of the `DELETEITEMSTRUCT` structure belongs to a combo box or list box, then the `DeleteItem` virtual function of the appropriate class is called. Override the `DeleteItem` member function of the appropriate control's class to delete item-specific data.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::DeleteString](../vs140/CComboBox--DeleteString.md)   
 [CListBox::DeleteString](../vs140/CListBox--DeleteString.md)   
 [CComboBox::ResetContent](../vs140/CComboBox--ResetContent.md)   
 [CListBox::ResetContent](../vs140/CListBox--ResetContent.md)   
 [WM_DELETEITEM](http://msdn.microsoft.com/library/windows/desktop/bb761362)   
 [CListBox::DeleteItem](../vs140/CListBox--DeleteItem.md)   
 [CComboBox::DeleteItem](../vs140/CComboBox--DeleteItem.md)