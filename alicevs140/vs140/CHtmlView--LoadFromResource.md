---
title: "CHtmlView::LoadFromResource"
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
ms.assetid: 1cac4a08-eac8-4f43-a78b-4788cb2236de
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::LoadFromResource
Call this member function to load the specified resource into the WebBrowser control.  
  
## Syntax  
  
```  
  
      BOOL LoadFromResource(  
   LPCTSTR lpszResource   
);  
BOOL LoadFromResource(  
   UINT nRes   
);  
```  
  
#### Parameters  
 `lpszResource`  
 A pointer to a string containing the name of the resource to load.  
  
 `nRes`  
 The ID of the buffer containing the name of the resource to load.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 Applies to Internet Explorer and WebBrowser.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)