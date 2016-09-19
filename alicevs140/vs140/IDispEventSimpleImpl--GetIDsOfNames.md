---
title: "IDispEventSimpleImpl::GetIDsOfNames"
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
ms.assetid: 07aa30cd-fdc9-4856-9bc6-3ced5d0ff5e8
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDispEventSimpleImpl::GetIDsOfNames
This implementation of **IDispatch::GetIDsOfNames** returns **E_NOTIMPL**.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetIDsOfNames)(  
   REFIID /* riid */,  
   LPOLESTR* /* rgszNames */,  
   UINT /* cNames */,  
   LCID /* lcid */,  
   DISPID* /* rgdispid */   
);  
```  
  
## Remarks  
 See [IDispatch::GetIDsOfNames](assetId:///6f6cf233-3481-436e-8d6a-51f93bf91619) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IDispEventSimpleImpl Class](../vs140/IDispEventSimpleImpl-Class.md)