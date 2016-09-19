---
title: "IRunnableObjectImpl::GetRunningClass"
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
ms.assetid: f98fd4ce-9ba1-4b3f-8f6f-faabd6e3654b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRunnableObjectImpl::GetRunningClass
Returns the CLSID of the running control.  
  
## Syntax  
  
```  
  
      HRESULT GetRunningClass(  
   LPCLSID lpClsid   
);  
```  
  
## Return Value  
 The ATL implementation sets \**lpClsid* to `GUID_NULL` and returns **E_UNEXPECTED**.  
  
## Remarks  
 See [IRunnableObject::GetRunningClass](http://msdn.microsoft.com/library/windows/desktop/ms693734) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IRunnableObjectImpl Class](../vs140/IRunnableObjectImpl-Class.md)