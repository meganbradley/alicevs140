---
title: "CDC::GetFontLanguageInfo"
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
ms.assetid: d55d7e89-7616-4eaf-9a76-1ee7ba4f440d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetFontLanguageInfo
Returns information about the currently selected font for the specified display context.  
  
## Syntax  
  
```  
  
DWORD GetFontLanguageInfo( ) const;  
  
```  
  
## Return Value  
 The return value identifies characteristics of the currently selected font. For a complete listing of possible values, see [GetFontLanguageInfo](http://msdn.microsoft.com/library/windows/desktop/dd144886).  
  
## Remarks  
 This member function emulates the functionality of the function [GetFontLanguageInfo](http://msdn.microsoft.com/library/windows/desktop/dd144886), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)