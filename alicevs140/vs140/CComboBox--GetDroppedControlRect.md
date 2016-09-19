---
title: "CComboBox::GetDroppedControlRect"
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
ms.assetid: f332ed8c-bcbf-4670-9855-c9ffd3afe9ed
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetDroppedControlRect
Call the `GetDroppedControlRect` member function to retrieve the screen coordinates of the visible (dropped-down) list box of a drop-down combo box.  
  
## Syntax  
  
```  
  
      void GetDroppedControlRect(  
   LPRECT lprect   
) const;  
```  
  
#### Parameters  
 *lprect*  
 Points to the [RECT](../vs140/RECT-Structure.md) structure that is to receive the coordinates.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#16)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CB_GETDROPPEDCONTROLRECT](http://msdn.microsoft.com/library/windows/desktop/bb775847)