---
title: "CAtlFileMappingBase::CAtlFileMappingBase"
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
ms.assetid: 7451bb15-e60c-45f5-80d1-549b04891886
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFileMappingBase::CAtlFileMappingBase
The constructor.  
  
## Syntax  
  
```  
  
      CAtlFileMappingBase(  
   CAtlFileMappingBase& orig   
);  
CAtlFileMappingBase( ) throw( );  
```  
  
#### Parameters  
 `orig`  
 The original file-mapping object to copy to create the new object.  
  
## Remarks  
 Creates a new file-mapping object, optionally using an existing object. It is still necessary to call [CAtlFileMappingBase::MapFile](../vs140/CAtlFileMappingBase--MapFile.md) to open or create the file-mapping object for a particular file.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#71](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#71)]  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFileMappingBase Class](../vs140/CAtlFileMappingBase-Class.md)