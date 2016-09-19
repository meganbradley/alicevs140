---
title: "COleServerDoc::OnFrameWindowActivate"
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
ms.assetid: 5a15a8bd-8b5b-4a18-8921-5f95d860cb18
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::OnFrameWindowActivate
The framework calls this function when the container application's frame window is activated or deactivated.  
  
## Syntax  
  
```  
  
      virtual void OnFrameWindowActivate(  
   BOOL bActivate   
);  
```  
  
#### Parameters  
 `bActivate`  
 Specifies whether the frame window is to be activated or deactivated.  
  
## Remarks  
 The default implementation cancels any help modes the frame window might be in. Override this function if you want to perform special processing when the frame window is activated or deactivated.  
  
 For more information, see the article [Activation](../vs140/Activation--C---.md)..  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::OnDocWindowActivate](../vs140/COleServerDoc--OnDocWindowActivate.md)