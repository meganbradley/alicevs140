---
title: "Asynchronous Monikers on the Internet"
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
ms.topic: article
ms.assetid: 418b0c64-0046-4dae-8118-c9c762b5822e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Asynchronous Monikers on the Internet
The Internet requires new approaches to application design because of its slow network access. Applications should perform network access asynchronously to avoid stalling the user interface. The MFC class [CAsyncMonikerFile](../vs140/CAsyncMonikerFile-Class.md) provides asynchronous support for downloading files.  
  
 With asynchronous monikers, you can extend your COM application to download asynchronously across the Internet and to provide progressive rendering of large objects such as bitmaps and VRML objects. Asynchronous monikers enable an ActiveX control property or a file on the Internet to be downloaded without blocking the response of the user interface.  
  
## Advantages of Asynchronous Monikers  
 You can use asynchronous monikers to:  
  
-   Download code and files without blocking.  
  
-   Download properties in ActiveX controls without blocking.  
  
-   Receive notifications of downloading progress.  
  
-   Track progress and ready state information.  
  
-   Provide status information to the user about progress.  
  
-   Allow the user to cancel a download at any time.  
  
## MFC Classes for Asynchronous Monikers  
 [CAsyncMonikerFile](../vs140/CAsyncMonikerFile-Class.md) is derived from [CMonikerFile](../vs140/CMonikerFile-Class.md), which in turn is derived from [COleStreamFile](../vs140/COleStreamFile-Class.md). A `COleStreamFile` object represents a stream of data; a `CMonikerFile` object uses an `IMoniker` to obtain the data, and a `CAsyncMonikerFile` object does so asynchronously.  
  
 Asynchronous monikers are used primarily in Internet-enabled applications and ActiveX controls to provide a responsive user interface during file transfers. A prime example of this is the use of [CDataPathProperty](../vs140/CDataPathProperty-Class.md) to provide asynchronous properties for ActiveX controls.  
  
## MFC Classes for Data Paths in ActiveX Controls  
 The MFC classes `CDataPathProperty` and [CCachedDataPathProperty](../vs140/CCachedDataPathProperty-Class.md) implement ActiveX control properties that can be loaded asynchronously. Asynchronous properties are loaded after synchronous initiation. Asynchronous ActiveX controls repeatedly invoke a callback to indicate availability of new data during a lengthy property exchange process.  
  
 `CDataPathProperty` is derived from `CAsyncMonikerFile`. `CCachedDataPathProperty` is derived from `CDataPathProperty`. To implement asynchronous properties in your ActiveX controls, derive a class from `CDataPathProperty` or `CCachedDataPathProperty`, and override [OnDataAvailable](../vs140/CAsyncMonikerFile--OnDataAvailable.md) and other notifications you wish to receive.  
  
#### To download a file using asynchronous monikers  
  
1.  Declare a class derived from [CAsyncMonikerFile](../vs140/CAsyncMonikerFile-Class.md).  
  
2.  Override [OnDataAvailable](../vs140/CAsyncMonikerFile--OnDataAvailable.md) to display the data.  
  
3.  Override other member functions, including [OnProgress](../vs140/CAsyncMonikerFile--OnProgress.md), [OnStartBinding](../vs140/CAsyncMonikerFile--OnStartBinding.md), and [OnStopBinding](../vs140/CAsyncMonikerFile--OnStopBinding.md).  
  
4.  Declare an instance of this class and use it to open URLs.  
  
 For information about downloading asynchronously in an ActiveX control, see [ActiveX Controls on the Internet](../vs140/ActiveX-Controls-on-the-Internet.md).  
  
## See Also  
 [MFC Internet Programming Tasks](../vs140/MFC-Internet-Programming-Tasks.md)   
 [MFC Internet Programming Basics](../vs140/MFC-Internet-Programming-Basics.md)