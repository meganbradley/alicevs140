---
title: "CDHtmlDialog::GetExternal"
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
ms.assetid: 8b9ef23b-24ab-4a45-beab-de8a549fe978
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::GetExternal
Gets the host's `IDispatch` interface.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetExternal)(  
   IDispatch **ppDispatch  
);  
```  
  
#### Parameters  
 *ppDispatch*  
 See *ppDispatch* in [IDocHostUIHandler::GetExternal](https://msdn.microsoft.com/en-us/library/aa753256.aspx) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 Returns `S_OK` on success or **E_NOTIMPL** on failure.  
  
## Remarks  
 This member function is CDHtmlDialog's implementation of [IDocHostUIHandler::GetExternal](https://msdn.microsoft.com/en-us/library/aa753256.aspx), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IDocHostUIhandler Interface](https://msdn.microsoft.com/en-us/library/aa753260.aspx)   
 [CDHtmlDialog::CanAccessExternal](../vs140/CDHtmlDialog--CanAccessExternal.md)   
 [CDHtmlDialog::SetExternalDispatch](../vs140/CDHtmlDialog--SetExternalDispatch.md)