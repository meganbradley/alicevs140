---
title: "COleControl::DisplayError"
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
ms.assetid: d25c5c06-7ecc-44ce-8989-875986e3d948
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::DisplayError
Called by the framework after the stock Error event has been handled (unless the event handler has suppressed the display of the error).  
  
## Syntax  
  
```  
  
      virtual void DisplayError(  
   SCODE scode,  
   LPCTSTR lpszDescription,  
   LPCTSTR lpszSource,  
   LPCTSTR lpszHelpFile,  
   UINT nHelpID   
);  
```  
  
#### Parameters  
 *scode*  
 The status code value to be reported. For a complete list of possible codes, see the article [ActiveX Controls: Advanced Topics](../vs140/MFC-ActiveX-Controls--Advanced-Topics.md).  
  
 `lpszDescription`  
 The description of the error being reported.  
  
 *lpszSource*  
 The name of the module generating the error (typically, the name of the OLE control module).  
  
 `lpszHelpFile`  
 The name of the help file containing a description of the error.  
  
 `nHelpID`  
 The Help Context ID of the error being reported.  
  
## Remarks  
 The default behavior displays a message box containing the description of the error, contained in `lpszDescription`.  
  
 Override this function to customize how errors are displayed.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::FireError](../vs140/COleControl--FireError.md)