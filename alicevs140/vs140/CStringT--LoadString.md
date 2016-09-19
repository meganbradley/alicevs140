---
title: "CStringT::LoadString"
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
ms.assetid: 2d5053e3-3b00-48e4-8ea6-a35bfec6445e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::LoadString
Reads a Windows string resource, identified by `nID`, into an existing `CStringT` object.  
  
## Syntax  
  
```  
BOOL LoadString(  
   HINSTANCE hInstance,  
   UINT nID,  
   WORD wLanguageID  
);  
BOOL LoadString(  
   HINSTANCE hInstance,  
   UINT nID  
);  
BOOL LoadString(  
   UINT nID  
);  
```  
  
#### Parameters  
 `hInstance`  
 A handle to the instance of the module.  
  
 `nID`  
 A Windows string resource ID.  
  
 `wLanguageID`  
 The language of the string resource.  
  
## Return Value  
 Nonzero if resource load was successful; otherwise 0.  
  
## Remarks  
 Loads the string resource (`nID`) from the specified module (`hInstance`) using the specified language (`wLanguage`).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#124](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#124)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)