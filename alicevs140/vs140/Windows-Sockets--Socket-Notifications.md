---
title: "Windows Sockets: Socket Notifications"
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
ms.assetid: 87d5bf70-6e77-49a9-9a64-aaadee2ad018
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Windows Sockets: Socket Notifications
This article describes the notification functions in the socket classes. These member functions are callback functions that the framework calls to notify your socket object of important events. The notification functions are:  
  
-   [OnReceive](../vs140/CAsyncSocket--OnReceive.md): Notifies this socket that there is data in the buffer for it to retrieve by calling [Receive](../vs140/CAsyncSocket--Receive.md).  
  
-   [OnSend](../vs140/CAsyncSocket--OnSend.md): Notifies this socket that it can now send data by calling [Send](../vs140/CAsyncSocket--Send.md).  
  
-   [OnAccept](../vs140/CAsyncSocket--OnAccept.md): Notifies this listening socket that it can accept pending connection requests by calling [Accept](../vs140/CAsyncSocket--Accept.md).  
  
-   [OnConnect](../vs140/CAsyncSocket--OnConnect.md): Notifies this connecting socket that its connection attempt completed: perhaps successfully or perhaps in error.  
  
-   [OnClose](../vs140/CAsyncSocket--OnClose.md): Notifies this socket that the socket it is connected to has closed.  
  
    > [!NOTE]
    >  An additional notification function is [OnOutOfBandData](../vs140/CAsyncSocket--OnOutOfBandData.md). This notification tells the receiving socket that the sending socket has "out-of-band" data to send. Out-of-band data is a logically independent channel associated with each pair of connected stream sockets. The out-of-band channel is typically used to send "urgent" data. MFC supports out-of-band data. Advanced users working with class [CAsyncSocket](../vs140/CAsyncSocket-Class.md) might need to use the out-of-band channel, but users of class [CSocket](../vs140/CSocket-Class.md) are discouraged from using it. The easier way is to create a second socket for passing such data. For more information about out-of-band data, see the Windows Sockets specification, available in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 If you derive from class `CAsyncSocket`, you must override the notification functions for those network events of interest to your application. If you derive a class from class `CSocket`, it is your choice whether to override the notification functions of interest. You can also use `CSocket` itself, in which case the notification functions default to doing nothing.  
  
 These functions are overridable callback functions. `CAsyncSocket` and `CSocket` convert messages to notifications, but you must implement how the notification functions respond if you wish to use them. The notification functions are called at the time your socket is notified of an event of interest, such as the presence of data to be read.  
  
 MFC calls the notification functions to let you customize your socket's behavior at the time it is notified. For example, you might call **Receive** from your `OnReceive` notification function, that is, on being notified that there is data to read, you call **Receive** to read it. This approach is not necessary, but it is a valid scenario. As an alternative, you might use your notification function to track progress, print **TRACE** messages, and so on.  
  
 You can take advantage of these notifications by overriding the notification functions in a derived socket class and providing an implementation.  
  
 During an operation such as receiving or sending data, a `CSocket` object becomes synchronous. During the synchronous state, any notifications meant for other sockets are queued while the current socket waits for the notification it wants. (For example, during a **Receive** call, the socket wants a notification to read.) Once the socket completes its synchronous operation and becomes asynchronous again, other sockets can begin receiving the queued notifications.  
  
> [!NOTE]
>  In `CSocket`, the `OnConnect` notification function is never called. For connections, you call **Connect**, which will return when the connection is completed (either successfully or in error). How connection notifications are handled is an MFC implementation detail.  
  
 For details about each notification function, see the function under class `CAsyncSocket` in the *MFC Reference*. For source code and information about MFC samples, see [MFC Samples](../vs140/Visual-C---Samples.md).  
  
 For more information, see:  
  
-   [Windows Sockets: Using Class CAsyncSocket](../vs140/Windows-Sockets--Using-Class-CAsyncSocket.md)  
  
-   [Windows Sockets: Deriving from Socket Classes](../vs140/Windows-Sockets--Deriving-from-Socket-Classes.md)  
  
-   [Windows Sockets: How Sockets with Archives Work](../vs140/Windows-Sockets--How-Sockets-with-Archives-Work.md)  
  
-   [Windows Sockets: Blocking](../vs140/Windows-Sockets--Blocking.md)  
  
-   [Windows Sockets: Byte Ordering](../vs140/Windows-Sockets--Byte-Ordering.md)  
  
-   [Windows Sockets: Converting Strings](../vs140/Windows-Sockets--Converting-Strings.md)  
  
## See Also  
 [Windows Sockets in MFC](../vs140/Windows-Sockets-in-MFC.md)