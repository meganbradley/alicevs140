---
title: "CAtlExeModuleT::WinMain"
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
ms.assetid: a4525dd5-fa67-420a-9603-709ae50b0381
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlExeModuleT::WinMain
This method implements the code required to run an EXE.  
  
## Syntax  
  
```  
  
      int WinMain(  
   int nShowCmd   
) throw( );  
```  
  
#### Parameters  
 `nShowCmd`  
 Specifies how the window is to be shown. This parameter can be one of the values discussed in the [WinMain](http://msdn.microsoft.com/library/windows/desktop/ms633559) section.  
  
## Return Value  
 Returns the executable's return value.  
  
## Remarks  
 This method can be overridden. If overriding [CAtlExeModuleT::PreMessageLoop](../vs140/CAtlExeModuleT--PreMessageLoop.md), [CAtlExeModuleT::PostMessageLoop](../vs140/CAtlExeModuleT--PostMessageLoop.md), or [CAtlExeModuleT::RunMessageLoop](../vs140/CAtlExeModuleT--RunMessageLoop.md) doesn't provide enough flexibility, it's possible to override the `WinMain` function using this method.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlExeModuleT Class](../vs140/CAtlExeModuleT-Class.md)   
 [WinMain](http://msdn.microsoft.com/library/windows/desktop/ms633559)