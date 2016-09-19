---
title: "CFile::SetFilePath"
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
ms.assetid: 3c655d99-b323-4f1d-bdc7-da282cbb5bfb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::SetFilePath
Call this function to specify the path of the file; for example, if the path of a file is not available when a [CFile](../vs140/CFile-Class.md) object is constructed, call `SetFilePath` to provide it.  
  
## Syntax  
  
```  
  
      virtual void SetFilePath(  
   LPCTSTR lpszNewName   
);  
```  
  
#### Parameters  
 `lpszNewName`  
 Pointer to a string specifying the new path.  
  
## Remarks  
  
> [!NOTE]
>  `SetFilePath` does not open the file or create the file; it simply associates the `CFile` object with a path name, which can then be used.  
  
## Example  
 [!CODE [NVC_MFCFiles#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#20)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::GetFilePath](../vs140/CFile--GetFilePath.md)   
 [CFile::CFile](../vs140/CFile--CFile.md)