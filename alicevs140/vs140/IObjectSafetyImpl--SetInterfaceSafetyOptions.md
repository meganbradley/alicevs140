---
title: "IObjectSafetyImpl::SetInterfaceSafetyOptions"
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
ms.assetid: 87a98c07-16d5-49df-b41e-6cbf7fe87b1b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IObjectSafetyImpl::SetInterfaceSafetyOptions
Makes the object safe for initialization or scripting by setting the [m_dwCurrentSafety](../vs140/IObjectSafetyImpl--m_dwCurrentSafety.md) member to the appropriate value.  
  
## Syntax  
  
```  
  
      HRESULT SetInterfaceSafetyOptions(  
   REFIID riid,  
   DWORD dwOptionsSetMask,  
   DWORD dwEnabledOptions   
);  
```  
  
## Remarks  
 The implementation returns **E_NOINTERFACE** for any interface not supported by the object's implementation of **IUnknown::QueryInterface**.  
  
> [!IMPORTANT]
>  Any object that supports `IObjectSafety` is responsible for its own security, and that of any object it delegates. The programmer must take into account issues arising from running code in the user's context, cross-site scripting and perform suitable zone checking.  
  
 See [IObjectSafety::SetInterfaceSafetyOptions](https://msdn.microsoft.com/en-us/library/aa768225.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IObjectSafetyImpl Class](../vs140/IObjectSafetyImpl-Class.md)   
 [IObjectSafetyImpl::GetInterfaceSafetyOptions](../vs140/IObjectSafetyImpl--GetInterfaceSafetyOptions.md)