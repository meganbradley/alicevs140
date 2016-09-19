---
title: "HSE_VERSION_INFO Structure"
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
ms.assetid: 4837312d-68c8-4d05-9afa-1934d7d49b20
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HSE_VERSION_INFO Structure
This structure is pointed to by the `pVer` parameter in the `CHttpServer::GetExtensionVersion` member function. It provides the ISA version number and a text description of the ISA.  
  
## Syntax  
  
```  
  
      typedef struct _HSE_VERSION_INFO {  
   DWORD dwExtensionVersion;  
   CHAR lpszExtensionDesc[HSE_MAX_EXT_DLL_NAME_LEN];  
} HSE_VERSION_INFO, *LPHSE_VERSION_INFO;  
```  
  
#### Parameters  
 *dwExtensionVersion*  
 The version number of the ISA.  
  
 *lpszExtensionDesc*  
 The text description of the ISA. The default implementation provides placeholder text; override `CHttpServer::GetExtensionVersion` to provide your own description.  
  
## Requirements  
 **Header:** httpext.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)