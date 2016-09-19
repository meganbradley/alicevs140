---
title: "CHtmlView::SetSilent"
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
ms.assetid: 40be4e9a-a5ec-4245-a3ff-476dceb81f99
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::SetSilent
Call this member function to set a value indicating whether any dialog boxes can be shown.  
  
## Syntax  
  
```  
  
      void SetSilent(  
   BOOL bNewValue   
);  
```  
  
#### Parameters  
 `bNewValue`  
 If nonzero, dialog boxes will not be displayed; if zero, dialog boxes will be displayed. The default value is zero.  
  
## Remarks  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetSilent](../vs140/CHtmlView--GetSilent.md)   
 [IWebBrowser2::put_Silent](https://msdn.microsoft.com/en-us/library/aa768269.aspx)