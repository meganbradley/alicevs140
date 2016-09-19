---
title: "Avoiding Exceptions on CLR Shutdown When Consuming COM Objects Built with -clr"
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
ms.topic: article
H1: Avoiding Exceptions on CLR Shutdown When Consuming COM Objects Built with /clr
ms.assetid: 41249d83-4b51-4e46-866f-27f475f2498c
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Avoiding Exceptions on CLR Shutdown When Consuming COM Objects Built with -clr
Once the common language runtime (CLR) enters shutdown mode, native functions have limited access to CLR services. When attempting to call Release on a COM object compiled with **/clr**, the CLR transitions to native code and then transitions back into managed code to service the IUnknown::Release call (which is defined in managed code). The CLR prevents the call back into managed code since it is in shutdown mode.  
  
 To resolve this, ensure that destructors called from Release methods only contain native code.  
  
## See Also  
 [Mixed Assemblies](../vs140/Mixed--Native-and-Managed--Assemblies.md)