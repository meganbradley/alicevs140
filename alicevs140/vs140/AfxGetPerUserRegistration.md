---
title: "AfxGetPerUserRegistration"
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
ms.topic: article
ms.assetid: 87c8536e-c9af-46e2-b2f2-f406c1fd12af
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetPerUserRegistration
Use this function to determine whether the application redirects registry access to the **HKEY_CURRENT_USER** (**HKCU**) node.  
  
## Syntax  
  
```  
BOOL AFXAPI AfxGetPerUserRegistration();  
```  
  
## Return Value  
 `TRUE` indicates that the registry information is directed to the **HKCU** node; `FALSE` indicates that the application writes registry information to the default node. The default node is **HKEY_CLASSES_ROOT** (**HKCR**).  
  
## Remarks  
 If you enable registry redirection, the framework redirects access from **HKCR** to **HKEY_CURRENT_USER\Software\Classes**. Only the MFC and ATL frameworks are affected by the redirection.  
  
 To change whether the application redirects registry access, use [AfxSetPerUserRegistration](../vs140/AfxSetPerUserRegistration.md).  
  
## Requirements  
 `Header:` afxstat_.h  
  
## See Also  
 [Macros, Global Functions, and Global Variables](../vs140/Macros--Global-Functions--and-Global-Variables.md)   
 [AfxSetPerUserRegistration](../vs140/AfxSetPerUserRegistration.md)   
 [Application Information and Management](../vs140/Application-Information-and-Management.md)