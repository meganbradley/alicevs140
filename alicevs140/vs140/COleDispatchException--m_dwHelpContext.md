---
title: "COleDispatchException::m_dwHelpContext"
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
ms.assetid: 4dd046ea-c5c8-4073-b665-6ecc93f06663
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchException::m_dwHelpContext
Identifies a help context in your application's help (.HLP) file.  
  
## Syntax  
  
```  
  
DWORD m_dwHelpContext;  
```  
  
## Remarks  
 This member is set by the function [AfxThrowOleDispatchException](../vs140/AfxThrowOleDispatchException.md) when an exception is thrown.  
  
## Example  
 See the example for [COleDispatchDriver::CreateDispatch](../vs140/COleDispatchDriver--CreateDispatch.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleDispatchException Class](../vs140/COleDispatchException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDispatchException::m_strDescription](../vs140/COleDispatchException--m_strDescription.md)   
 [COleDispatchException::m_wCode](../vs140/COleDispatchException--m_wCode.md)   
 [AfxThrowOleDispatchException](../vs140/AfxThrowOleDispatchException.md)