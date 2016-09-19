---
title: "CComControlBase::GetAmbientTextAlign"
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
ms.assetid: 0c27c78b-d9c7-424f-b70f-574745b835e3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComControlBase::GetAmbientTextAlign
Retrieves **DISPID_AMBIENT_TEXTALIGN**, the text alignment preferred by the container: 0 for general alignment (numbers right, text left), 1 for left alignment, 2 for center alignment, and 3 for right alignment.  
  
## Syntax  
  
```  
  
      HRESULT GetAmbientTextAlign(  
   short& nTextAlign   
);   
```  
  
#### Parameters  
 *nTextAlign*  
 The property **DISPID_AMBIENT_TEXTALIGN**.  
  
## Return Value  
 One of the standard HRESULT values.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CComControlBase Class](../vs140/CComControlBase-Class.md)