---
title: "IDataObjectImpl::DUnadvise"
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
ms.assetid: 71ace0eb-bc04-4ba9-92f2-c584446e0ada
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDataObjectImpl::DUnadvise
Terminates a connection previously established through [DAdvise](../vs140/IDataObjectImpl--DAdvise.md).  
  
## Syntax  
  
```  
  
      HRESULT DUnadvise(  
   DWORD dwConnection   
);  
```  
  
## Remarks  
 See [IDataObject::DUnadvise](http://msdn.microsoft.com/library/windows/desktop/ms692448) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IDataObjectImpl Class](../vs140/IDataObjectImpl-Class.md)   
 [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177)   
 [IAdviseSink](http://msdn.microsoft.com/library/windows/desktop/ms692513)