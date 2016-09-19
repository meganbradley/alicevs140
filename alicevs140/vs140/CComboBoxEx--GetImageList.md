---
title: "CComboBoxEx::GetImageList"
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
ms.assetid: b10fe333-c8e4-4009-9ecf-50f38b7be6cb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBoxEx::GetImageList
Call this member function to get a pointer to the image list used by a `CComboBoxEx` control.  
  
## Syntax  
  
```  
  
CImageList* GetImageList( ) const;  
  
```  
  
## Return Value  
 A pointer to a [CImageList](../vs140/CImageList-Class.md) object. If it fails, this member function returns **NULL**.  
  
## Remarks  
 The `CImageList` object pointed to by the return value is a temporary object and is destroyed during the next idle processing time.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CComboBoxEx Class](../vs140/CComboBoxEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBoxEx::SetImageList](../vs140/CComboBoxEx--SetImageList.md)   
 [COMBOBOXEXITEM](http://msdn.microsoft.com/library/windows/desktop/bb775746)