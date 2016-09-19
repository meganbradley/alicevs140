---
title: "CDocument::ReportSaveLoadException"
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
ms.assetid: 45b348bf-a972-4e5f-a315-65419732ac22
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::ReportSaveLoadException
Called if an exception is thrown (typically a [CFileException](../vs140/CFileException-Class.md) or [CArchiveException](../vs140/CArchiveException-Class.md)) while saving or loading the document.  
  
## Syntax  
  
```  
  
      virtual void ReportSaveLoadException(  
   LPCTSTR lpszPathName,  
   CException* e,  
   BOOL bSaving,  
   UINT nIDPDefault   
);  
```  
  
#### Parameters  
 `lpszPathName`  
 Points to name of document that was being saved or loaded.  
  
 *e*  
 Points to the exception that was thrown. May be **NULL**.  
  
 *bSaving*  
 Flag indicating what operation was in progress; nonzero if the document was being saved, 0 if the document was being loaded.  
  
 `nIDPDefault`  
 Identifier of the error message to be displayed if the function does not specify a more specific one.  
  
## Remarks  
 The default implementation examines the exception object and looks for an error message that specifically describes the cause. If a specific message is not found or if *e* is **NULL**, the general message specified by the `nIDPDefault` parameter is used. The function then displays a message box containing the error message. Override this function if you want to provide additional, customized failure messages. This is an advanced overridable.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::OnOpenDocument](../vs140/CDocument--OnOpenDocument.md)   
 [CDocument::OnSaveDocument](../vs140/CDocument--OnSaveDocument.md)   
 [CFileException Class](../vs140/CFileException-Class.md)   
 [CArchiveException Class](../vs140/CArchiveException-Class.md)