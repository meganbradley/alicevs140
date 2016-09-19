---
title: "CMFCDropDownToolbarButton::OnChangeParentWnd"
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
ms.assetid: 7085ec96-e182-43c4-9162-f901e9c2cba5
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::OnChangeParentWnd
Called by the framework when the button is inserted into a new toolbar.  
  
## Syntax  
  
```  
virtual void OnChangeParentWnd(  
   CWnd* pWndParent  
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 The new parent window.  
  
## Remarks  
 This method overrides the base class implementation ([CMFCToolBarButton::OnChangeParentWnd](../vs140/CMFCToolBarButton--OnChangeParentWnd.md)) by clearing the text label ([CMFCToolBarButton::m_strText](../vs140/CMFCToolBarButton--m_strText.md)) and setting the [CMFCToolBarButton::m_bText](../vs140/CMFCToolBarButton--m_bText.md) and [CMFCToolBarButton::m_bUserButton](../vs140/CMFCToolBarButton--m_bUserButton.md) data members to `FALSE`.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnChangeParentWnd](../vs140/CMFCToolBarButton--OnChangeParentWnd.md)   
 [CMFCToolBarButton::m_strText](../vs140/CMFCToolBarButton--m_strText.md)   
 [CMFCToolBarButton::m_bText](../vs140/CMFCToolBarButton--m_bText.md)   
 [CMFCToolBarButton::m_bUserButton](../vs140/CMFCToolBarButton--m_bUserButton.md)