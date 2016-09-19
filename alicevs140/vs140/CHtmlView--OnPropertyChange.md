---
title: "CHtmlView::OnPropertyChange"
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
ms.assetid: dd95a425-4c9a-4ab4-8353-3a367fe1e048
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnPropertyChange
This member function is called by the framework to notify an application that [PutProperty](../vs140/CHtmlView--PutProperty.md) has changed the value of a property.  
  
## Syntax  
  
```  
  
      virtual void OnPropertyChange(  
   LPCTSTR lpszProperty   
);  
```  
  
#### Parameters  
 `lpszProperty`  
 A pointer to a string containing the name of the property.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetProperty](../vs140/CHtmlView--GetProperty.md)