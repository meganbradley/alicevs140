---
title: "COleServerDoc::COleServerDoc"
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
ms.assetid: 7726aafa-1da1-410f-8e1b-0378c8242544
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::COleServerDoc
Constructs a `COleServerDoc` object without connecting with the OLE system DLLs.  
  
## Syntax  
  
```  
  
COleServerDoc( );  
```  
  
## Remarks  
 You must call [COleLinkingDoc::Register](../vs140/COleLinkingDoc--Register.md) to open communications with OLE. If you are using [COleTemplateServer](../vs140/COleTemplateServer-Class.md) in your application, `COleLinkingDoc::Register` is called for you by `COleLinkingDoc`'s implementation of `OnNewDocument`, `OnOpenDocument`, and `OnSaveDocument`.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleLinkingDoc::Register](../vs140/COleLinkingDoc--Register.md)