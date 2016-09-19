---
title: "CMutex Class"
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
ms.assetid: 6330c050-4f01-4195-a099-2029b92f8cf1
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMutex Class
Represents a "mutex" — a synchronization object that allows one thread mutually exclusive access to a resource.  
  
## Syntax  
  
```  
class CMutex : public CSyncObject  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CMutex::CMutex](#cmutex__cmutex)|Constructs a `CMutex` object.|  
  
## Remarks  
 Mutexes are useful when only one thread at a time can be allowed to modify data or some other controlled resource. For example, adding nodes to a linked list is a process that should only be allowed by one thread at a time. By using a `CMutex` object to control the linked list, only one thread at a time can gain access to the list.  
  
 To use a `CMutex` object, construct the `CMutex` object when it is needed. Specify the name of the mutex you wish to wait on, and that your application should initially own it. You can then access the mutex when the constructor returns. Call [CSyncObject::Unlock](../vs140/CSyncObject-Class.md#csyncobject__unlock) when you are done accessing the controlled resource.  
  
 An alternative method for using `CMutex` objects is to add a variable of type `CMutex` as a data member to the class you wish to control. During construction of the controlled object, call the constructor of the `CMutex` data member specifying if the mutex is initially owned, the name of the mutex (if it will be used across process boundaries), and desired security attributes.  
  
 To access resources controlled by `CMutex` objects in this manner, first create a variable of either type [CSingleLock](../vs140/CSingleLock-Class.md) or type [CMultiLock](../vs140/CMultiLock-Class.md) in your resource's access member function. Then call the lock object's `Lock` member function (for example, [CSingleLock::Lock](../vs140/CSingleLock-Class.md#csinglelock__lock)). At this point, your thread will either gain access to the resource, wait for the resource to be released and gain access, or wait for the resource to be released and time out, failing to gain access to the resource. In any case, your resource has been accessed in a thread-safe manner. To release the resource, use the lock object's `Unlock` member function (for example, [CSingleLock::Unlock](../vs140/CSingleLock-Class.md#csinglelock__unlock)), or allow the lock object to fall out of scope.  
  
 For more information on using `CMutex` objects, see the article [Multithreading: How to Use the Synchronization Classes](../vs140/Multithreading--How-to-Use-the-Synchronization-Classes.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CSyncObject](../vs140/CSyncObject-Class.md)  
  
 `CMutex`  
  
## Requirements  
 **Header:** afxmt.h  
  
##  <a name="cmutex__cmutex"></a>  CMutex::CMutex  
 Constructs a named or unnamed `CMutex` object.  
  
```  
CMutex(    BOOL bInitiallyOwn  = FALSE,    LPCTSTR  lpszName  = NULL,    LPSECURITY_ATTRIBUTES lpsaAttribute  = NULL );  
  
```  
  
### Parameters  
 `bInitiallyOwn`  
 Specifies if the thread creating the `CMutex` object initially has access to the resource controlled by the mutex.  
  
 `lpszName`  
 Name of the `CMutex` object. If another mutex with the same name exists, `lpszName` must be supplied if the object will be used across process boundaries. If **NULL**, the mutex will be unnamed. If the name matches an existing mutex, the constructor builds a new `CMutex` object which references the mutex of that name. If the name matches an existing synchronization object that is not a mutex, the construction will fail.  
  
 `lpsaAttribute`  
 Security attributes for the mutex object. For a full description of this structure, see                                 [SECURITY_ATTRIBUTES](http://msdn.microsoft.com/library/windows/desktop/aa379560) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
### Remarks  
 To access or release a `CMutex` object, create a [CMultiLock](../vs140/CMultiLock-Class.md) or [CSingleLock](../vs140/CSingleLock-Class.md) object and call its [Lock](../vs140/CSingleLock-Class.md#csinglelock__lock) and [Unlock](../vs140/CSingleLock-Class.md#csinglelock__unlock) member functions. If the `CMutex` object is being used stand-alone, call its `Unlock` member function to release it.  
  
> [!IMPORTANT]
>  After creating the `CMutex` object, use                             [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) to ensure that the mutex did not already exist. If the mutex did exist unexpectedly, it may indicate a rogue process is squatting and may be intending to use the mutex maliciously. In this case, the recommended security-conscious procedure is to close the handle and continue as if there was a failure in creating the object.  
  
## See Also  
 [Base Class](../vs140/CSyncObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)