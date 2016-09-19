---
title: "IDataObjectImpl::SetData"
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
ms.assetid: a525dfff-1f7b-43f7-9d99-0c5e06d73192
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDataObjectImpl::SetData
Transfers data from the client to the data object.  
  
## Syntax  
  
```  
  
      HRESULT SetData(  
   FORMATETC* pformatetc,  
   STGMEDIUM* pmedium,  
   BOOL fRelease   
);  
```  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 See [IDataObject::SetData](http://msdn.microsoft.com/library/windows/desktop/ms686626) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IDataObjectImpl Class](../vs140/IDataObjectImpl-Class.md)   
 [IDataObjectImpl::GetData](../vs140/IDataObjectImpl--GetData.md)   
 [IDataObjectImpl::GetDataHere](../vs140/IDataObjectImpl--GetDataHere.md)   
 [IDataObjectImpl::QueryGetData](../vs140/IDataObjectImpl--QueryGetData.md)   
 [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177)   
 [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812)