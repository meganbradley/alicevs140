---
title: "IDataObjectImpl::GetDataHere"
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
ms.assetid: 180f2eb1-ddc1-4344-a693-0cfa24c0cbdb
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDataObjectImpl::GetDataHere
Similar to `GetData`, except the client must allocate the **STGMEDIUM** structure.  
  
## Syntax  
  
```  
  
      HRESULT GetDataHere(  
   FORMATETC* pformatetc,  
   STGMEDIUM* pmedium   
);  
```  
  
## Return Value  
 Returns **E_NOTIMPL**.  
  
## Remarks  
 See [IDataObject::GetDataHere](http://msdn.microsoft.com/library/windows/desktop/ms687266) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IDataObjectImpl Class](../vs140/IDataObjectImpl-Class.md)   
 [IDataObjectImpl::GetData](../vs140/IDataObjectImpl--GetData.md)   
 [IDataObjectImpl::QueryGetData](../vs140/IDataObjectImpl--QueryGetData.md)   
 [IDataObjectImpl::SetData](../vs140/IDataObjectImpl--SetData.md)   
 [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177)   
 [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812)