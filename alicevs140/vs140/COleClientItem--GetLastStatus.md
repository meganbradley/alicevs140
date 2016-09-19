---
title: "COleClientItem::GetLastStatus"
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
ms.assetid: 5f7ab6a9-2545-4733-b713-107c28e9c653
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetLastStatus
Returns the status code of the last OLE operation.  
  
## Syntax  
  
```  
  
SCODE GetLastStatus( ) const;  
```  
  
## Return Value  
 An `SCODE` value.  
  
## Remarks  
 For member functions that return a **BOOL** value of **FALSE**, or other member functions that return **NULL**, `GetLastStatus` returns more detailed failure information. Be aware that most OLE member functions throw exceptions for more serious errors. The specific information on the interpretation of the `SCODE` depends on the underlying OLE call that last returned an `SCODE` value.  
  
 For more information on `SCODE`, see [Structure of COM Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms690088) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] documentation.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)