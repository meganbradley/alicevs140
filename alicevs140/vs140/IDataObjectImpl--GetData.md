---
title: "IDataObjectImpl::GetData"
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
ms.assetid: 092f55d5-efbd-45d9-a862-f37c5adcfd1e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDataObjectImpl::GetData
Transfers data from the data object to the client.  
  
## Syntax  
  
```  
  
      HRESULT GetData(  
   FORMATETC* pformatetcIn,  
   STGMEDIUM* pmedium   
);  
```  
  
## Remarks  
 The *pformatetcIn* parameter must specify a storage medium type of **TYMED_MFPICT**.  
  
 See [IDataObject::GetData](http://msdn.microsoft.com/library/windows/desktop/ms678431) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IDataObjectImpl Class](../vs140/IDataObjectImpl-Class.md)   
 [IDataObjectImpl::GetDataHere](../vs140/IDataObjectImpl--GetDataHere.md)   
 [IDataObjectImpl::QueryGetData](../vs140/IDataObjectImpl--QueryGetData.md)   
 [IDataObjectImpl::SetData](../vs140/IDataObjectImpl--SetData.md)   
 [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177)   
 [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms683812)   
 [TYMED](http://msdn.microsoft.com/library/windows/desktop/ms691227)