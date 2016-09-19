---
title: "CDC::StartDoc"
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
ms.assetid: 46f816f0-589d-4f90-8a3a-d0ce90a8a3ab
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::StartDoc
Informs the device driver that a new print job is starting and that all subsequent `StartPage` and `EndPage` calls should be spooled under the same job until an `EndDoc` call occurs.  
  
## Syntax  
  
```  
  
      int StartDoc(  
   LPDOCINFO lpDocInfo   
);  
int StartDoc(  
   LPCTSTR lpszDocName   
);  
```  
  
#### Parameters  
 *lpDocInfo*  
 Points to a [DOCINFO](http://msdn.microsoft.com/library/windows/desktop/dd183574) structure containing the name of the document file and the name of the output file.  
  
 *lpszDocName*  
 Pointer to a string containing the name of the document file.  
  
## Return Value  
 If the function succeeds, the return value is greater than zero. This value is the print job identifier for the document.  
  
 If the function fails, the return value is less than or equal to zero.  
  
## Remarks  
 This ensures that documents longer than one page will not be interspersed with other jobs.  
  
 For Windows versions 3.1 and later, this function replaces the **STARTDOC** printer escape. Using this function ensures that documents containing more than one page are not interspersed with other print jobs.  
  
 `StartDoc` should not be used inside metafiles.  
  
## Example  
 This code fragment gets the default printer, opens a print job, and spools one page with "Hello, World!" on it. Because the text printed by this code isn't scaled to the printer's logical units, the output text may be in such small letters that the result is unreadable. The CDC scaling functions, such as `SetMapMode`, `SetViewportOrg`, and `SetWindowExt`, can be used to fix the scaling.  
  
 [!CODE [NVC_MFCDocView#41](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#41)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Escape](../vs140/CDC--Escape.md)   
 [CDC::EndDoc](../vs140/CDC--EndDoc.md)   
 [CDC::AbortDoc](../vs140/CDC--AbortDoc.md)