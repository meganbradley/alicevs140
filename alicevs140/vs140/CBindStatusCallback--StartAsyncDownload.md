---
title: "CBindStatusCallback::StartAsyncDownload"
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
ms.assetid: 6c8b2d79-b1be-4c6a-995d-af42fd26ab58
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::StartAsyncDownload
Starts downloading data asynchronously from the specified URL.  
  
## Syntax  
  
```  
  
      HRESULT StartAsyncDownload(  
   T* pT,  
   ATL_PDATAAVAILABLE pFunc,  
   BSTR bstrURL,  
   IUnknown* pUnkContainer = NULL,   
   BOOL bRelative = FALSE   
);  
```  
  
#### Parameters  
 *pT*  
 [in] A pointer to the object requesting the asynchronous data transfer. The `CBindStatusCallback` object is templatized on this object's class.  
  
 *pFunc*  
 [in] A pointer to the function that receives the data being read. The function is a member of your object's class of type `T`. See **Remarks** for syntax and an example.  
  
 `bstrURL`  
 [in] The URL to obtain data from. Can be any valid URL or file name. Cannot be **NULL**. For example:  
  
 `CComBSTR mybstr =_T("http://somesite/data.htm")`  
  
 `pUnkContainer`  
 [in] The **IUnknown** of the container. **NULL** by default.  
  
 `bRelative`  
 [in] A flag indicating whether the URL is relative or absolute. **FALSE** by default, meaning the URL is absolute.  
  
## Return Value  
 One of the standard `HRESULT` values.  
  
## Remarks  
 Every time data is available it is sent to the object through `OnDataAvailable`. `OnDataAvailable` reads the data and calls the function pointed to by *pFunc* (for example, to store the data or print it to the screen).  
  
 The function pointed to by *pFunc* is a member of your object's class and has the following syntax:  
  
 `void Function_Name(`  
  
 `CBindStatusCallback<T>*`  `pbsc` `,`  
  
 `BYTE*`  `pBytes` `,`  
  
 `DWORD`  `dwSize`  
  
 `);`  
  
 In the following example (taken from the [ASYNC](../vs140/Visual-C---Samples.md) sample), the function `OnData` writes the received data into a text box.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#87](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#87)]  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::OnDataAvailable](../vs140/CBindStatusCallback--OnDataAvailable.md)