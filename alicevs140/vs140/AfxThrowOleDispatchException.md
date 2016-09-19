---
title: "AfxThrowOleDispatchException"
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
ms.assetid: 500a4360-0528-4b2e-a129-956bfa8051fd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxThrowOleDispatchException
Use this function to throw an exception within an OLE automation function.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxThrowOleDispatchException(  
   WORD wCode,  
   LPCSTR lpszDescription,  
   UINT nHelpID = 0   
);  
void AFXAPI AfxThrowOleDispatchException(  
   WORD wCode,  
   UINT nDescriptionID,  
   UINT nHelpID =  -1   
);  
```  
  
#### Parameters  
 `wCode`  
 An error code specific to your application.  
  
 `lpszDescription`  
 Verbal description of the error.  
  
 `nDescriptionID`  
 Resource ID for the verbal error description.  
  
 `nHelpID`  
 A help context for your application's help (.HLP) file.  
  
## Remarks  
 The information provided to this function can be displayed by the driving application (Microsoft Visual Basic or another OLE automation client application).  
  
## Example  
 [!CODE [NVC_MFCExceptions#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCExceptions#25)]  
  
## Requirements  
 **Header:** <afxdisp.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [COleException Class](../vs140/COleException-Class.md)