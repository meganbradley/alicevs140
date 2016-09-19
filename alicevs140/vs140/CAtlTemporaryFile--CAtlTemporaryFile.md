---
title: "CAtlTemporaryFile::CAtlTemporaryFile"
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
ms.assetid: da56bc17-7450-4328-b0dd-1f103c725c9b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::CAtlTemporaryFile
The constructor.  
  
## Syntax  
  
```  
  
CAtlTemporaryFile( ) throw( );  
  
```  
  
## Remarks  
 A file is not actually opened until a call is made to [CAtlTemporaryFile::Create](../vs140/CAtlTemporaryFile--Create.md).  
  
## Example  
 [!CODE [NVC_ATL_Utilities#73](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#73)]  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)   
 [CAtlTemporaryFile::~CAtlTemporaryFile](../vs140/CAtlTemporaryFile--~CAtlTemporaryFile.md)