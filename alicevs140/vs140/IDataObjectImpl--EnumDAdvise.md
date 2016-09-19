---
title: "IDataObjectImpl::EnumDAdvise"
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
ms.assetid: e180c398-0904-469e-b25b-0352a0eba684
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDataObjectImpl::EnumDAdvise
Creates an enumerator to iterate through the current advisory connections.  
  
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
 See [IDataObject::EnumDAdvise](http://msdn.microsoft.com/library/windows/desktop/ms680127) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IDataObjectImpl Class](../vs140/IDataObjectImpl-Class.md)   
 [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177)   
 [IAdviseSink](http://msdn.microsoft.com/library/windows/desktop/ms692513)