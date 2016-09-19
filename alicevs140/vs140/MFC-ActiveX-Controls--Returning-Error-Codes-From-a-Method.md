---
title: "MFC ActiveX Controls: Returning Error Codes From a Method"
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
ms.assetid: 771fb9c9-2413-4dcc-b386-7bc4c4adeafd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC ActiveX Controls: Returning Error Codes From a Method
This article describes how to return error codes from an ActiveX control method.  
  
 To indicate that an error has occurred within a method, you should use the [COleControl::ThrowError](../vs140/COleControl--ThrowError.md) member function, which takes an `SCODE` (status code) as a parameter. You can use a predefined `SCODE` or define one of your own.  
  
> [!NOTE]
>  `ThrowError` is meant to be used only as a means of returning an error from within a property's Get or Set function or an automation Method. These are the only times that the appropriate exception handler will be present on the stack.  
  
 Helper functions exist for the most common predefined `SCODE`s, such as [COleControl::SetNotSupported](../vs140/COleControl--SetNotSupported.md), [COleControl::GetNotSupported](../vs140/COleControl--GetNotSupported.md), and [COleControl::SetNotPermitted](../vs140/COleControl--SetNotPermitted.md).  
  
 For a list of predefined `SCODE`s and instructions on defining custom `SCODE`s, see the section [Handling Errors in Your ActiveX Control](../vs140/MFC-ActiveX-Controls--Advanced-Topics.md) in ActiveX Controls: Advanced Topics.  
  
 For more information on reporting exceptions in other areas of your code, see [COleControl::FireError](../vs140/COleControl--FireError.md) and the section [Handling Errors in Your ActiveX Control](../vs140/MFC-ActiveX-Controls--Advanced-Topics.md) in ActiveX Controls: Advanced Topics.  
  
## See Also  
 [MFC ActiveX Controls](../vs140/MFC-ActiveX-Controls.md)