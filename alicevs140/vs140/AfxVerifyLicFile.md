---
title: "AfxVerifyLicFile"
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
ms.assetid: 9fad6b11-bd24-4be1-849a-04ae5ef90b41
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxVerifyLicFile
Call this function to verify that the license file named by `pszLicFileName` is valid for the OLE control.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxVerifyLicFile(  
   HINSTANCE hInstance,  
   LPCTSTR pszLicFileName,  
   LPOLESTR pszLicFileContents,  
   UINT cch = -1   
);  
```  
  
#### Parameters  
 `hInstance`  
 The instance handle of the DLL associated with the licensed control.  
  
 `pszLicFileName`  
 Points to a null-terminated character string containing the license filename.  
  
 `pszLicFileContents`  
 Points to a byte sequence that must match the sequence found at the beginning of the license file.  
  
 `cch`  
 Number of characters in `pszLicFileContents`.  
  
## Return Value  
 Nonzero if the license file exists and begins with the character sequence in `pszLicFileContents`; otherwise 0.  
  
## Remarks  
 If `cch` is – 1, this function uses:  
  
 [!CODE [NVC_MFC_Utilities#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#36)]  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [COleObjectFactory::VerifyUserLicense](../vs140/COleObjectFactory--VerifyUserLicense.md)