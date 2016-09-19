---
title: "CComboBoxEx::SetExtendedStyle"
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
ms.assetid: e9ee0d43-08d3-4520-bed8-7c1b19e606b6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBoxEx::SetExtendedStyle
Call this member function to set the extended styles used for a combo box extended control.  
  
## Syntax  
  
```  
  
      DWORD SetExtendedStyle(  
   DWORD dwExMask,  
   DWORD dwExStyles   
);  
```  
  
#### Parameters  
 `dwExMask`  
 A `DWORD` value that indicates which styles in `dwExStyles` are to be affected. Only the extended styles in `dwExMask` will be changed. All other styles will be maintained as is. If this parameter is zero, then all of the styles in `dwExStyles` will be affected.  
  
 `dwExStyles`  
 A `DWORD` value that contains the combo box control extended styles to set for the control.  
  
## Return Value  
 A `DWORD` value that contains the extended styles previously used for the control.  
  
## Remarks  
 See [ComboBoxEx Control Extended Styles](http://msdn.microsoft.com/library/windows/desktop/bb775742) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information about these styles.  
  
 To create a combo box extended control with extended windows styles, use [CreateEx](../vs140/CComboBoxEx--CreateEx.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CComboBoxEx Class](../vs140/CComboBoxEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBoxEx::GetExtendedStyle](../vs140/CComboBoxEx--GetExtendedStyle.md)