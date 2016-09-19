---
title: "afxDump (CDumpContext in MFC)"
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
ms.assetid: 4b3cfa3f-fb75-456a-9d99-a5601acbcb11
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# afxDump (CDumpContext in MFC)
Provides basic object-dumping capability in your application.  
  
## Syntax  
  
```  
  
CDumpContext afxDump;  
```  
  
## Remarks  
 `afxDump` is a predefined [CDumpContext](../vs140/CDumpContext-Class.md) object that allows you to send `CDumpContext` information to the debugger output window or to a debug terminal. Typically, you supply `afxDump` as a parameter to `CObject::Dump`.  
  
 Under Windows NT and all versions of Windows, `afxDump` output is sent to the Output-Debug window of Visual C++ when you debug your application.  
  
 This variable is defined only in the Debug version of MFC. For more information on `afxDump`, see [Debugging MFC Applications](../vs140/MFC-Debugging-Techniques.md).  
  
## Example  
 [!CODE [NVC_MFC_Utilities#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#23)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CObject::Dump](../vs140/CObject--Dump.md)   
 [AfxDump](../vs140/AfxDump--MFC-.md)