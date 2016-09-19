---
title: "CGopherFile::CGopherFile"
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
ms.assetid: 2035c041-3ebd-4ed3-aba6-96a6534e76d6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGopherFile::CGopherFile
This member function is called to construct a `CGopherFile` object.  
  
## Syntax  
  
```  
  
      CGopherFile(  
   HINTERNET hFile,  
   CGopherLocator& refLocator,  
   CGopherConnection* pConnection   
);  
CGopherFile(  
   HINTERNET hFile,  
   HINTERNET hSession,  
   LPCTSTR pstrLocator,  
   DWORD dwLocLen,  
   DWORD_PTR dwContext   
);  
```  
  
#### Parameters  
 `hFile`  
 A handle to an `HINTERNET` file.  
  
 `refLocator`  
 A reference to a [CGopherLocator](../vs140/CGopherLocator-Class.md) object.  
  
 `pConnection`  
 A pointer to a [CGopherConnection](../vs140/CGopherConnection-Class.md) object.  
  
 `hSession`  
 A handle to the current Internet session.  
  
 `pstrLocator`  
 A pointer to a string used to locate the gopher server. See [Gopher Sessions](_inet_Gopher_Sessions) for more information about gopher locators.  
  
 *dwLocLen*  
 A DWORD containing the number of bytes in `pstrLocator`.  
  
 `dwContext`  
 A pointer to the context identifier of the file being opened.  
  
## Remarks  
 You need a `CGopherFile` object to read from a file during a gopher Internet session.  
  
 You never create a `CGopherFile` object directly. Instead, call [CGopherConnection::OpenFile](../vs140/CGopherConnection--OpenFile.md) to open a file on a gopher server.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CGopherFile Class](../vs140/CGopherFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [CGopherLocator Class](../vs140/CGopherLocator-Class.md)   
 [CGopherFileFind Class](../vs140/CGopherFileFind-Class.md)   
 [CGopherConnection Class](../vs140/CGopherConnection-Class.md)