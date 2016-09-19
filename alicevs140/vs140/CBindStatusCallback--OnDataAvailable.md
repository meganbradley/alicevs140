---
title: "CBindStatusCallback::OnDataAvailable"
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
ms.assetid: a0a27b4e-ba93-482b-a7c3-2235e2310dde
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::OnDataAvailable
The system-supplied asynchronous moniker calls `OnDataAvailable` to provide data to the object as it becomes available.  
  
## Syntax  
  
```  
  
      STDMETHOD(OnDataAvailable)(  
   DWORD grfBSCF,  
   DWORD dwSize,  
   FORMATETC* /* pformatetc */,  
   STGMEDIUM* pstgmed   
);  
```  
  
#### Parameters  
 *grfBSCF*  
 [in] A **BSCF** enumeration value. One or more of the following: **BSCF_FIRSTDATANOTIFICATION**, **BSCF_INTERMEDIARYDATANOTIFICATION**, or **BSCF_LASTDATANOTIFICATION**.  
  
 `dwSize`  
 [in] The cumulative amount (in bytes) of data available since the beginning of the binding. Can be zero, indicating that the amount of data is not relevant or that no specific amount became available.  
  
 *pformatetc*  
 [in] Pointer to the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682242) structure that contains the format of the available data. If there is no format, can be **CF_NULL**.  
  
 *pstgmed*  
 [in] Pointer to the [STGMEDIUM](http://msdn.microsoft.com/library/windows/desktop/ms695269) structure that holds the actual data now available.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 `OnDataAvailable` reads the data, then calls a method of your object's class (for example, to store the data or print it to the screen). See [CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md) for details.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md)