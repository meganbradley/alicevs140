---
title: "CMonikerFile::Open"
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
ms.assetid: ec3ec682-8b41-409a-b6ab-da50ccf2be77
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonikerFile::Open
Call this member function to open a file or moniker object.  
  
## Syntax  
  
```  
  
      virtual BOOL Open(  
   LPCTSTR lpszURL,  
   CFileException* pError = NULL   
);  
virtual BOOL Open(  
   IMoniker* pMoniker,  
   CFileException* pError = NULL   
);  
```  
  
#### Parameters  
 `lpszURL`  
 A URL or filename of the file to be opened.  
  
 `pError`  
 A pointer to a file exception. In the event of an error, it will be set to the cause.  
  
 `pMoniker`  
 A pointer to the moniker interface `IMoniker` to be used to obtain a stream.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The `lpszURL` parameter cannot be used on a Macintosh. Only the `pMoniker` form of **Open** can be used on a Macintosh.  
  
 You can use a URL or a filename for the `lpszURL` parameter. For example:  
  
 [!CODE [NVC_MFCWinInet#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWinInet#6)]  
  
 – or –  
  
 [!CODE [NVC_MFCWinInet#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWinInet#7)]  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [CMonikerFile Class](../vs140/CMonikerFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonikerFile::CMonikerFile](../vs140/CMonikerFile--CMonikerFile.md)   
 [CAsyncMonikerFile::Open](../vs140/CAsyncMonikerFile--Open.md)