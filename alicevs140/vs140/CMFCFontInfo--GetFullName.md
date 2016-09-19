---
title: "CMFCFontInfo::GetFullName"
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
ms.assetid: 6427bb7a-1d09-4478-86a5-08c5c5486f90
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCFontInfo::GetFullName
Retrieves the concatenated names of a font and its character set (script).  
  
## Syntax  
  
```  
CString GetFullName() const;  
```  
  
## Return Value  
 A string that contains the font name and script.  
  
## Remarks  
 Use this method to obtain the full name of the font. For example, if the font name is is `Arial` and the font script is `Cyrillic`, this method returns "Arial (Cyrillic)".  
  
## Requirements  
 **Header:** afxtoolbarfontcombobox.h  
  
## See Also  
 [CMFCFontInfo Class](../vs140/CMFCFontInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)