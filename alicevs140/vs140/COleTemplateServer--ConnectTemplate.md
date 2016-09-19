---
title: "COleTemplateServer::ConnectTemplate"
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
ms.assetid: 09a2fb46-8bad-4d03-a5e8-3077f498f637
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleTemplateServer::ConnectTemplate
Connects the document template pointed to by `pDocTemplate` to the underlying [COleObjectFactory](../vs140/COleObjectFactory-Class.md) object.  
  
## Syntax  
  
```  
  
      void ConnectTemplate(  
   REFCLSID clsid,  
   CDocTemplate* pDocTemplate,  
   BOOL bMultiInstance   
);  
```  
  
#### Parameters  
 `clsid`  
 Reference to the OLE class ID that the template requests.  
  
 `pDocTemplate`  
 Pointer to the document template.  
  
 `bMultiInstance`  
 Indicates whether a single instance of the application can support multiple instantiations. If **TRUE**, multiple instances of the application are launched for each request to create an object.  
  
## Remarks  
 For more information, see [CLSID Key](http://msdn.microsoft.com/library/windows/desktop/ms691424) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleTemplateServer Class](../vs140/COleTemplateServer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)