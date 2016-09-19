---
title: "CDocTemplate::LoadTemplate"
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
ms.assetid: 6cdfe39e-e69d-4a29-a14c-8d833bff2239
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::LoadTemplate
Loads the resources for a given `CDocTemplate` or derived class.  
  
## Syntax  
  
```  
  
virtual void LoadTemplate( );  
  
```  
  
## Remarks  
 This member function is called by the framework to load the resources for a given `CDocTemplate` or derived class. Normally it is called during construction, except when the template is being constructed globally. In that case, the call to `LoadTemplate` is delayed until [CWinApp::AddDocTemplate](../vs140/CWinApp--AddDocTemplate.md) is called.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::AddDocTemplate](../vs140/CWinApp--AddDocTemplate.md)