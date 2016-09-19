---
title: "AfxInitRichEdit2"
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
ms.assetid: 4a21857b-e45e-429e-b41a-b09f77fec99f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxInitRichEdit2
Call this function to initialize the rich edit control (version 2.0 and later) for the application.  
  
## Syntax  
  
```  
  
BOOL AFXAPI AfxInitRichEdit2( );  
  
```  
  
## Remarks  
 Call this function to load the RICHED20.DLL and initialize version 2.0 of the rich edit control. If you call the Create method of [CRichEditCtrl](../vs140/CRichEditCtrl-Class.md), [CRichEditView](../vs140/CRichEditView-Class.md), or [CRichEditDoc](../vs140/CRichEditDoc-Class.md), you typically don't need to call this function, but in some cases it might be necessary.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [AfxInitRichEdit](../vs140/AfxInitRichEdit.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)