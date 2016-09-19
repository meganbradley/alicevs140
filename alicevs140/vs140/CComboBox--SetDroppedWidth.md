---
title: "CComboBox::SetDroppedWidth"
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
ms.assetid: 759462e0-4b4f-4cfe-a068-e876e4996852
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SetDroppedWidth
Call this function to set the minimum allowable width, in pixels, of the list box of a combo box.  
  
## Syntax  
  
```  
  
      int SetDroppedWidth(  
   UINT nWidth   
);  
```  
  
#### Parameters  
 `nWidth`  
 The minimum allowable width of the list-box portion of the combo box, in pixels.  
  
## Return Value  
 If successful, the new width of the list box, otherwise **CB_ERR**.  
  
## Remarks  
 This function only applies to combo boxes with the [CBS_DROPDOWN](../vs140/Combo-Box-Styles.md) or [CBS_DROPDOWNLIST](../vs140/Combo-Box-Styles.md) style.  
  
 By default, the minimum allowable width of the drop-down list box is 0. When the list-box portion of the combo box is displayed, its width is the larger of the minimum allowable width or the combo box width.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#34)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetDroppedWidth](../vs140/CComboBox--GetDroppedWidth.md)   
 [CB_SETDROPPEDWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb775901)