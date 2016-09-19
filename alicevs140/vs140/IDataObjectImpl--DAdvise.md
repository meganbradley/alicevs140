---
title: "IDataObjectImpl::DAdvise"
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
ms.assetid: 80baa6e4-caca-43c9-be80-acf938f9ac3e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDataObjectImpl::DAdvise
Establishes a connection between the data object and an advise sink.  
  
## Syntax  
  
```  
  
      HRESULT DAdvise(  
   FORMATETC* pformatetc,  
   DWORD advf,  
   IAdviseSink* pAdvSink,  
   DWORD* pdwConnection   
);  
```  
  
## Remarks  
 This enables the advise sink to receive notifications of changes in the object.  
  
 To terminate the connection, call [DUnadvise](../vs140/IDataObjectImpl--DUnadvise.md).  
  
 See [IDataObject::DAdvise](http://msdn.microsoft.com/library/windows/desktop/ms692579) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IDataObjectImpl Class](../vs140/IDataObjectImpl-Class.md)   
 [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177)   
 [IAdviseSink](http://msdn.microsoft.com/library/windows/desktop/ms692513)