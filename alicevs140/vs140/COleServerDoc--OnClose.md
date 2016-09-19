---
title: "COleServerDoc::OnClose"
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
ms.assetid: 41b90af3-1f6f-4cc2-a4f0-0309266fce88
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::OnClose
Called by the framework when a container requests that the server document be closed.  
  
## Syntax  
  
```  
  
      virtual void OnClose(  
   OLECLOSE dwCloseOption   
);  
```  
  
#### Parameters  
 `dwCloseOption`  
 A value from the enumeration `OLECLOSE`. This parameter can have one of the following values:  
  
-   `OLECLOSE_SAVEIFDIRTY` The file is saved if it has been modified.  
  
-   `OLECLOSE_NOSAVE` The file is closed without being saved.  
  
-   `OLECLOSE_PROMPTSAVE` If the file has been modified, the user is prompted about saving it.  
  
## Remarks  
 The default implementation calls `CDocument::OnCloseDocument`.  
  
 For more information and additional values, see [OLECLOSE](http://msdn.microsoft.com/library/windows/desktop/ms680623) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleException Class](../vs140/COleException-Class.md)   
 [CDocument::OnCloseDocument](../vs140/CDocument--OnCloseDocument.md)