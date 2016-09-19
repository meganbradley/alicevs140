---
title: "CComboBoxEx::Create"
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
ms.assetid: dceb97aa-47f6-4094-a906-7e49d1970eea
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBoxEx::Create
Creates the combo box and attaches it to the `CComboBoxEx` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID   
);  
```  
  
#### Parameters  
 `dwStyle`  
 Specifies the combination of combo box styles applied to the combo box. See **Remarks** below for more information about styles.  
  
 `rect`  
 A reference to a [CRect](../vs140/CRect-Class.md) object or [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure, which is the position and size of the combo box.  
  
 `pParentWnd`  
 A pointer to a [CWnd](../vs140/CWnd-Class.md) object that is the parent window of the combo box (usually a `CDialog`). It must not be **NULL**.  
  
 `nID`  
 Specifies the combo box's control ID.  
  
## Return Value  
 Nonzero if the object was created successfully; otherwise 0.  
  
## Remarks  
 Create a `CComboBoxEx` object in two steps:  
  
1.  Call [CComboBoxEx](../vs140/CComboBoxEx--CComboBoxEx.md) to construct a `CComboBoxEx` object.  
  
2.  Call this member function, which creates the extended Windows combo box and attaches it to the `CComboBoxEx` object.  
  
 When you call **Create**, MFC initializes the common controls.  
  
 When you create the combo box, you can specify any or all of the following combo-box styles:  
  
-   **CBS_SIMPLE**  
  
-   **CBS_DROPDOWN**  
  
-   **CBS_DROPDOWNLIST**  
  
-   **CBS_AUTOHSCROLL**  
  
-   **WS_CHILD**  
  
 All other styles passed when you create the window are ignored. The **ComboBoxEx** control also supports extended styles that provide additional features. These styles are described in [ComboBoxEx control extended styles](http://msdn.microsoft.com/library/windows/desktop/bb775742), in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. Set these styles by calling [SetExtendedStyle](../vs140/CComboBoxEx--SetExtendedStyle.md).  
  
 If you want to use extended windows styles with your control, call [CreateEx](../vs140/CComboBoxEx--CreateEx.md) instead of **Create**.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CComboBoxEx Class](../vs140/CComboBoxEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBoxEx::CComboBoxEx](../vs140/CComboBoxEx--CComboBoxEx.md)