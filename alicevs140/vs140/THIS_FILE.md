---
title: "THIS_FILE"
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
ms.assetid: 68c147ab-c696-4b20-80a4-5e6db2b15132
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# THIS_FILE
Expands to the name of the file that is being compiled.  
  
## Syntax  
  
```  
  
THIS_FILE  
  
```  
  
## Remarks  
 The information is used by the **ASSERT** and **VERIFY** macros. The Application Wizard and code wizards place the macro in source code files they create.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#35](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#35)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ASSERT](../vs140/ASSERT--MFC-.md)   
 [VERIFY](../vs140/VERIFY.md)