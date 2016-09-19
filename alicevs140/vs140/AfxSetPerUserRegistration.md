---
title: "AfxSetPerUserRegistration"
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
ms.assetid: f4795761-0c4d-4d5b-bbeb-d8351be77143
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxSetPerUserRegistration
Sets whether the application redirects registry access to the **HKEY_CURRENT_USER** (**HKCU**) node.  
  
## Syntax  
  
```  
void AFXAPI AfxSetPerUserRegistration(  
   BOOL bEnable  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` indicates that the registry information is directed to the **HKCU** node; `FALSE` indicates that the application writes registry information to the default node. The default node is **HKEY_CLASSES_ROOT** (**HKCR**).  
  
## Remarks  
 Before [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)], applications that access the registry usually use the **HKEY_CLASSES_ROOT** node. However, with [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)], you must run an application in elevated mode to write to **HKCR**.  
  
 This method enables your application to read and write to the registry without running in elevated mode by redirecting registry access from **HKCR** to **HKCU**. For more information, see [Linker Property Pages](../Topic/Linker%20Property%20Pages.md).  
  
 If you enable registry redirection, the framework redirects access from **HKCR** to **HKEY_CURRENT_USER\Software\Classes**. Only the MFC and ATL frameworks are affected by the redirection.  
  
 The default implementation accesses the registry under **HKCR**.  
  
## Requirements  
 `Header:` afxstat_.h  
  
## See Also  
 [Macros, Global Functions, and Global Variables](../vs140/Macros--Global-Functions--and-Global-Variables.md)   
 [AfxGetPerUserRegistration](../vs140/AfxGetPerUserRegistration.md)   
 [Application Information and Management](../vs140/Application-Information-and-Management.md)