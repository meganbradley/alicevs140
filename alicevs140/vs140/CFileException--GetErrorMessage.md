---
title: "CFileException::GetErrorMessage"
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
ms.assetid: 42a8379e-ae53-4c8a-94d0-8628cefd5a3c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileException::GetErrorMessage
Retrieves text that describes an exception.  
  
## Syntax  
  
```  
virtual BOOL GetErrorMessage(  
   LPTSTR lpszError,  
   UINT nMaxError,  
   PUINT pnHelpContext = NULL   
) const;  
```  
  
#### Parameters  
 [in, out] `lpszError`  
 Pointer to a buffer that receives an error message.  
  
 [in] `nMaxError`  
 The maximum number of characters the specified buffer can hold. This includes the terminating null character.  
  
 [in, out] `pnHelpContext`  
 Pointer to an unsigned integer that receives the help context ID. If `NULL`, no ID is returned.  
  
## Return Value  
 `TRUE` if the method was successful; otherwise `FALSE`.  
  
## Remarks  
 If the specified buffer is too small, the error message is truncated.  
  
## Example  
 The following example uses `CFileException::GetErrorMessage`.  
  
 [!CODE [NVC_MFCExceptions#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCExceptions#22)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CException Class](../vs140/CException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CException::ReportError](../vs140/CException--ReportError.md)