---
title: "COlePropertiesDialog::m_psh"
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
ms.assetid: 52ef3ead-8d14-4829-9fa8-e7dc8eb3494a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertiesDialog::m_psh
A structure of type [PROPSHEETHEADER](http://msdn.microsoft.com/library/windows/desktop/bb774546), whose members store the characteristics of the dialog object.  
  
## Syntax  
  
```  
  
PROPSHEETHEADER m_psh;  
  
```  
  
## Remarks  
 After constructing a `COlePropertiesDialog` object, you can use `m_psh` to set various aspects of the dialog box before calling the `DoModal` member function.  
  
 If you modify the `m_psh` data member directly, you will override any default behavior.  
  
 For more information on the **PROPSHEETHEADER** structure, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePropertiesDialog Class](../vs140/COlePropertiesDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePropertiesDialog::DoModal](../vs140/COlePropertiesDialog--DoModal.md)