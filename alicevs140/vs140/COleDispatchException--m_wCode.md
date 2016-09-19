---
title: "COleDispatchException::m_wCode"
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
ms.assetid: 53886b7f-cf3a-44c0-a1df-1f4dfec65e74
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchException::m_wCode
Contains an error code specific to your application.  
  
## Syntax  
  
```  
  
WORD m_wCode;  
```  
  
## Remarks  
 This member is set by the function [AfxThrowOleDispatchException](../vs140/AfxThrowOleDispatchException.md) when an exception is thrown.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleDispatchException Class](../vs140/COleDispatchException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDispatchException::m_strDescription](../vs140/COleDispatchException--m_strDescription.md)   
 [COleDispatchException::m_dwHelpContext](../vs140/COleDispatchException--m_dwHelpContext.md)   
 [AfxThrowOleDispatchException](../vs140/AfxThrowOleDispatchException.md)