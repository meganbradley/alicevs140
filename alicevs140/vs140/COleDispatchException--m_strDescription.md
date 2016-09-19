---
title: "COleDispatchException::m_strDescription"
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
ms.assetid: 03326be7-b43d-46eb-b78c-0de34ce453c0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDispatchException::m_strDescription
Contains a verbal error description, such as "Disk full."  
  
## Syntax  
  
```  
  
CString m_strDescription;  
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
 [COleDispatchException::m_dwHelpContext](../vs140/COleDispatchException--m_dwHelpContext.md)   
 [COleDispatchException::m_wCode](../vs140/COleDispatchException--m_wCode.md)   
 [AfxThrowOleDispatchException](../vs140/AfxThrowOleDispatchException.md)