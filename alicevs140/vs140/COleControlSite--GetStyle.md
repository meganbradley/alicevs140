---
title: "COleControlSite::GetStyle"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 18d36cc4-97d1-4b66-93d5-ec6c1bcc47c0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlSite::GetStyle
Retrieves the styles of the control site.  
  
## Syntax  
  
```  
  
virtual DWORD GetStyle( ) const;  
  
```  
  
## Return Value  
 The window's styles.  
  
## Remarks  
 For a list of possible values, see [Windows Styles](../vs140/Window-Styles.md). To retrieve the extended styles of the control site, call [COleControlSite::GetExStyle](../vs140/COleControlSite--GetExStyle.md).  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlSite Class](../vs140/COleControlSite-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)