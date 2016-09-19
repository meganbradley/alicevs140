---
title: "IProvideClassInfo2Impl::GetGUID"
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
ms.assetid: 881e468a-9182-4c4e-83fb-a70f5a403774
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IProvideClassInfo2Impl::GetGUID
Retrieves the GUID for the object's outgoing dispinterface.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetGUID)(  
   DWORD dwGuidKind,  
   GUID* pGUID   
);  
```  
  
## Remarks  
 See [IProvideClassInfo2::GetGUID](http://msdn.microsoft.com/library/windows/desktop/ms679721) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IProvideClassInfo2Impl Class](../vs140/IProvideClassInfo2Impl-Class.md)