---
title: "CComboBox::GetLocale"
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
ms.assetid: 4398ead0-9921-4817-acf0-58405a29d918
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetLocale
Retrieves the locale used by the combo box.  
  
## Syntax  
  
```  
  
LCID GetLocale( ) const;  
```  
  
## Return Value  
 The locale identifier (LCID) value for the strings in the combo box.  
  
## Remarks  
 The locale is used, for example, to determine the sort order of the strings in a sorted combo box.  
  
## Example  
 See the example for [CComboBox::SetLocale](../vs140/CComboBox--SetLocale.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SetLocale](../vs140/CComboBox--SetLocale.md)   
 [GetStringTypeW](http://msdn.microsoft.com/library/windows/desktop/dd318119)   
 [GetSystemDefaultLCID](http://msdn.microsoft.com/library/windows/desktop/dd318121)   
 [GetUserDefaultLCID](http://msdn.microsoft.com/library/windows/desktop/dd318135)