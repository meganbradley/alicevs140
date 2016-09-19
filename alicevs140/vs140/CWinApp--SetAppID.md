---
title: "CWinApp::SetAppID"
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
ms.assetid: c1b634b4-9a78-4faa-9338-ec1d77f8c96c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::SetAppID
Explicitly sets Application User Model ID for the application. This method should be called before any user interface is presented to the user (the best place is the application constructor).  
  
## Syntax  
  
```  
void SetAppID(  
   LPCTSTR lpcszAppID  
);  
```  
  
#### Parameters  
 `lpcszAppID`  
 Specifies the Application User Model ID.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)