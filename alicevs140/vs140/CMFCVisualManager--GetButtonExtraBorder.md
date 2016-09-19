---
title: "CMFCVisualManager::GetButtonExtraBorder"
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
ms.assetid: f51b0aea-0218-45fe-9cca-63d5be04e742
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::GetButtonExtraBorder
The framework calls this method when it draws a toolbar button.  
  
## Syntax  
  
```  
virtual CSize GetButtonExtraBorder() const;  
```  
  
## Return Value  
 A [CSize](../vs140/CSize-Class.md) object that contains the extra size of the border for toolbar buttons.  
  
## Remarks  
 Some skins have to extend the borders of toolbar buttons. Override this method in a custom visual manager to extend the borders of toolbar buttons in your application. The default implementation of this method returns an empty size.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)