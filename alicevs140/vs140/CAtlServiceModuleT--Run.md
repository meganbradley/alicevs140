---
title: "CAtlServiceModuleT::Run"
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
ms.assetid: b4f8d570-d81b-4c57-b5d6-8308c70df0d7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlServiceModuleT::Run
Runs the service.  
  
## Syntax  
  
```  
  
      HRESULT Run(  
   int nShowCmd = SW_HIDE   
) throw( );  
```  
  
#### Parameters  
 `nShowCmd`  
 Specifies how the window is to be shown. This parameter can be one of the values discussed in the [WinMain](http://msdn.microsoft.com/library/windows/desktop/ms633559) section. The default value is SW_HIDE.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 After being called, **Run** calls [CAtlServiceModuleT::PreMessageLoop](../vs140/CAtlServiceModuleT--PreMessageLoop.md), [CAtlExeModuleT::RunMessageLoop](../vs140/CAtlExeModuleT--RunMessageLoop.md), and [CAtlExeModuleT::PostMessageLoop](../vs140/CAtlExeModuleT--PostMessageLoop.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlServiceModuleT Class](../vs140/CAtlServiceModuleT-Class.md)