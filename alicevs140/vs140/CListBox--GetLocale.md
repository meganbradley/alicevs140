---
title: "CListBox::GetLocale"
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
ms.assetid: c24b8f50-2aaf-45ce-9847-1c30d1148597
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetLocale
Retrieves the locale used by the list box.  
  
## Syntax  
  
```  
  
LCID GetLocale( ) const;  
```  
  
## Return Value  
 The locale identifier (LCID) value for the strings in the list box.  
  
## Remarks  
 The locale is used, for example, to determine the sort order of the strings in a sorted list box.  
  
## Example  
 See the example for [CListBox::SetLocale](../vs140/CListBox--SetLocale.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::SetLocale](../vs140/CListBox--SetLocale.md)   
 [GetStringTypeW](http://msdn.microsoft.com/library/windows/desktop/dd318119)   
 [GetSystemDefaultLCID](http://msdn.microsoft.com/library/windows/desktop/dd318121)   
 [GetUserDefaultLCID](http://msdn.microsoft.com/library/windows/desktop/dd318135)