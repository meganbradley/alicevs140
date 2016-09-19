---
title: "AFX_EXT_CLASS"
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
ms.assetid: b8685760-6c2f-4445-9613-9753d37bd0fc
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_EXT_CLASS
[Extension DLLs](../vs140/Extension-DLLs--Overview.md) use the macro **AFX_EXT_CLASS** to export classes; the executables that link to the extension DLL use the macro to import classes.  
  
## Remarks  
 With the **AFX_EXT_CLASS** macro, the same header file(s) used to build the extension DLL can be used with the executables that link to the DLL.  
  
 In the header file for your DLL, add the **AFX_EXT_CLASS** keyword to the declaration of your class as follows:  
  
 [!CODE [NVC_MFC_DLL#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_DLL#1)]  
  
 For more information, see [Export and Import Using AFX_EXT_CLASS](../vs140/Exporting-and-Importing-Using-AFX_EXT_CLASS.md).  
  
## Requirements  
 Header: **afxv_**dll.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)