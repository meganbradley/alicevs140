---
title: "IPropertyPageImpl::Activate"
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
ms.assetid: e9486c5d-e70a-4801-9168-f6a0eb9dd813
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IPropertyPageImpl::Activate
Creates the dialog box window for the property page.  
  
## Syntax  
  
```  
  
      HRESULT Activate(  
   HWND hWndParent,  
   LPCRECT pRect,  
   BOOL bModal   
);  
```  
  
## Remarks  
 By default, the dialog box is always modeless, regardless of the value of the *bModal* parameter.  
  
 See [IPropertyPage::Activate](http://msdn.microsoft.com/library/windows/desktop/ms682250) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IPropertyPageImpl Class](../vs140/IPropertyPageImpl-Class.md)   
 [IPropertyPageImpl::Deactivate](../vs140/IPropertyPageImpl--Deactivate.md)