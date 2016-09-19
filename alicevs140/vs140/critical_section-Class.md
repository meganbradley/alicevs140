---
title: "critical_section Class"
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
ms.assetid: fa3c89d6-be5d-4d1b-bddb-8232814e6cf6
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# critical_section Class
A non-reentrant mutex which is explicitly aware of the Concurrency Runtime.  
  
## Syntax  
  
```  
class critical_section;  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`native_handle_type`|A reference to a                                         `critical_section` object.|  
  
### Public Classes  
  
|Name|Description|  
|----------|-----------------|  
|[critical_section::scoped_lock Class](#critical_section__scoped_lock_class)|An exception safe RAII wrapper for a                                         `critical_section` object.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[critical_section::critical_section Constructor](#critical_section__critical_section_constructor)|Constructs a new critical section.|  
|[critical_section::~critical_section Destructor](#critical_section___dtorcritical_section_destructor)|Destroys a critical section.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[critical_section::lock Method](#critical_section__lock_method)|Acquires this critical section.|  
|[critical_section::native_handle Method](#critical_section__native_handle_method)|Returns a platform specific native handle, if one exists.|  
|[critical_section::try_lock Method](#critical_section__try_lock_method)|Tries to acquire the lock without blocking.|  
|[critical_section::try_lock_for Method](#critical_section__try_lock_for_method)|Tries to acquire the lock without blocking for a specific number of milliseconds.|  
|[critical_section::unlock Method](#critical_section__unlock_method)|Unlocks the critical section.|  
  
## Remarks  
 For more information, see                 [Synchronization Data Structures](../vs140/Synchronization-Data-Structures.md).  
  
## Inheritance Hierarchy  
 `critical_section`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="critical_section__critical_section_constructor"></a>  critical_section::critical_section Constructor  
 Constructs a new critical section.  
  
```  
critical_section();  
```  
  
##  <a name="critical_section___dtorcritical_section_destructor"></a>  critical_section::~critical_section Destructor  
 Destroys a critical section.  
  
```  
~critical_section();  
```  
  
### Remarks  
 It is expected that the lock is no longer held when the destructor runs. Allowing the critical section to destruct with the lock still held results in undefined behavior.  
  
##  <a name="critical_section__lock_method"></a>  critical_section::lock Method  
 Acquires this critical section.  
  
```  
void lock();  
```  
  
### Remarks  
 It is often safer to utilize the                         [scoped_lock](#critical_section__scoped_lock_class) construct to acquire and release a                         `critical_section` object in an exception safe way.  
  
 If the lock is already held by the calling context, an                         [improper_lock](../vs140/improper_lock-Class.md) exception will be thrown.  
  
##  <a name="critical_section__native_handle_method"></a>  critical_section::native_handle Method  
 Returns a platform specific native handle, if one exists.  
  
```  
native_handle_type native_handle();  
```  
  
### Return Value  
 A reference to the critical section.  
  
### Remarks  
 A                         `critical_section` object is not associated with a platform specific native handle for the Windows operating system. The method simply returns a reference to the object itself.  
  
##  <a name="critical_section__scoped_lock_class"></a>  critical_section::scoped_lock Class  
 An exception safe RAII wrapper for a                 `critical_section` object.  
  
```  
class scoped_lock;  
```  
  
##  <a name="critical_section__try_lock_method"></a>  critical_section::try_lock Method  
 Tries to acquire the lock without blocking.  
  
```  
bool try_lock();  
```  
  
### Return Value  
 If the lock was acquired, the value                         `true`; otherwise, the value                         `false`.  
  
##  <a name="critical_section__try_lock_for_method"></a>  critical_section::try_lock_for Method  
 Tries to acquire the lock without blocking for a specific number of milliseconds.  
  
```  
bool try_lock_for(  
   unsigned int                 _Timeout  
);  
```  
  
### Parameters  
 `_Timeout`  
 The number of milliseconds to wait before timing out.  
  
### Return Value  
 If the lock was acquired, the value                         `true`; otherwise, the value                         `false`.  
  
##  <a name="critical_section__unlock_method"></a>  critical_section::unlock Method  
 Unlocks the critical section.  
  
```  
void unlock();  
```  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [reader_writer_lock Class](../vs140/reader_writer_lock-Class.md)