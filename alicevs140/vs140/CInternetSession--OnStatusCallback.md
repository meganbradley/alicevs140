---
title: "CInternetSession::OnStatusCallback"
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
ms.assetid: cf123163-eb5c-4c9c-87ae-de8cf22eb5c3
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetSession::OnStatusCallback
This member function is called by the framework to update the status when status callback is enabled and an operation is pending.  
  
## Syntax  
  
```  
  
      virtual void OnStatusCallback(  
   DWORD_PTR dwContext,  
   DWORD dwInternetStatus,  
   LPVOID lpvStatusInformation,  
   DWORD dwStatusInformationLength   
);  
```  
  
#### Parameters  
 `dwContext`  
 The context value supplied by the application.  
  
 `dwInternetStatus`  
 A status code which indicates why the callback is being made. See **Remarks** for a table of possible values.  
  
 `lpvStatusInformation`  
 A pointer to a buffer containing information pertinent to this callback.  
  
 `dwStatusInformationLength`  
 The size of `lpvStatusInformation`.  
  
## Remarks  
 You must first call [EnableStatusCallback](../vs140/CInternetSession--EnableStatusCallback.md) to take advantage of status callback.  
  
 The `dwInternetStatus` parameter indicates the operation being performed and determines what the contents of `lpvStatusInformation` will be. `dwStatusInformationLength` indicates the length of the data included in `lpvStatusInformation`. The following status values for `dwInternetStatus` are defined as follows:  
  
|Value|Meaning|  
|-----------|-------------|  
|`INTERNET_STATUS_RESOLVING_NAME`|Looking up the IP address of the name contained in `lpvStatusInformation`.|  
|`INTERNET_STATUS_NAME_RESOLVED`|Successfully found the IP address of the name contained in `lpvStatusInformation`.|  
|`INTERNET_STATUS_CONNECTING_TO_SERVER`|Connecting to the socket address ([SOCKADDR](../vs140/SOCKADDR-Structure.md)) pointed to by `lpvStatusInformation`.|  
|`INTERNET_STATUS_CONNECTED_TO_SERVER`|Successfully connected to the socket address (`SOCKADDR`) pointed to by `lpvStatusInformation`.|  
|`INTERNET_STATUS_SENDING_REQUEST`|Sending the information request to the server. The `lpvStatusInformation` parameter is **NULL**.|  
|**INTERNET_STATUS_ REQUEST_SENT**|Successfully sent the information request to the server. The `lpvStatusInformation` parameter is **NULL**.|  
|`INTERNET_STATUS_RECEIVING_RESPONSE`|Waiting for the server to respond to a request. The `lpvStatusInformation` parameter is **NULL**.|  
|`INTERNET_STATUS_RESPONSE_RECEIVED`|Successfully received a response from the server. The `lpvStatusInformation` parameter is **NULL**.|  
|`INTERNET_STATUS_CLOSING_CONNECTION`|Closing the connection to the server. The `lpvStatusInformation` parameter is **NULL**.|  
|`INTERNET_STATUS_CONNECTION_CLOSED`|Successfully closed the connection to the server. The `lpvStatusInformation` parameter is **NULL**.|  
|`INTERNET_STATUS_HANDLE_CREATED`|Used by the Win32 API function [InternetConnect](http://msdn.microsoft.com/library/windows/desktop/aa384363) to indicate that it has created the new handle. This lets the application call the Win32 function [InternetCloseHandle](http://msdn.microsoft.com/library/windows/desktop/aa384350) from another thread if the connect is taking too long. See the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]for more information about these functions.|  
|`INTERNET_STATUS_HANDLE_CLOSING`|Successfully terminated this handle value.|  
  
 Override this member function to require some action before a status callback routine is performed.  
  
> [!NOTE]
>  Status callbacks need thread-state protection. If you are using MFC in a shared library, add the following line to the beginning of your override:  
  
 [!CODE [NVC_MFCHtmlHttp#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCHtmlHttp#8)]  
  
 For more information about asynchronous operations, see the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetSession Class](../vs140/CInternetSession-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetSession::EnableStatusCallback](../vs140/CInternetSession--EnableStatusCallback.md)   
 [CInternetSession::GetContext](../vs140/CInternetSession--GetContext.md)