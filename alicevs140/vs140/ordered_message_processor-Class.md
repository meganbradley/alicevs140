---
title: "ordered_message_processor Class"
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
ms.assetid: 787adfb7-7f79-4a70-864a-80e3b64088cd
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ordered_message_processor Class
An             `ordered_message_processor` is a             `message_processor` that allows message blocks to process messages in the order they were received.  
  
## Syntax  
  
```  
template<  
   class             _Type  
>  
class ordered_message_processor : public message_processor<            _Type>;  
```  
  
#### Parameters  
 `_Type`  
 The payload type of messages handled by the processor.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`type`|A type alias for                                         `_Type`.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[ordered_message_processor::ordered_message_processor Constructor](#ordered_message_processor__ordered_message_processor_constructor)|Constructs an                                         `ordered_message_processor` object.|  
|[ordered_message_processor::~ordered_message_processor Destructor](#ordered_message_processor___dtorordered_message_processor_destructor)|Destroys the                                         `ordered_message_processor` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ordered_message_processor::async_send Method](#ordered_message_processor__async_send_method)|Asynchronously queues up messages and starts a processing task, if this has not been done already. (Overrides                                         [message_processor::async_send](../vs140/message_processor-Class.md#message_processor__async_send_method).)|  
|[ordered_message_processor::initialize Method](#ordered_message_processor__initialize_method)|Initializes the                                         `ordered_message_processor` object with the appropriate callback function, scheduler and schedule group.|  
|[ordered_message_processor::initialize_batched_processing Method](#ordered_message_processor__initialize_batched_processing_method)|Initialize batched message processing|  
|[ordered_message_processor::sync_send Method](#ordered_message_processor__sync_send_method)|Synchronously queues up messages and starts a processing task, if this has not been done already. (Overrides                                         [message_processor::sync_send](../vs140/message_processor-Class.md#message_processor__sync_send_method).)|  
|[ordered_message_processor::wait Method](#ordered_message_processor__wait_method)|A processor-specific spin wait used in destructors of message blocks to make sure that all asynchronous processing tasks have time to finish before destroying the block. (Overrides                                         [message_processor::wait](../vs140/message_processor-Class.md#message_processor__wait_method).)|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ordered_message_processor::process_incoming_message Method](#ordered_message_processor__process_incoming_message_method)|The processing function that is called asynchronously. It dequeues messages and begins processing them. (Overrides                                         [message_processor::process_incoming_message](../vs140/message_processor-Class.md#message_processor__process_incoming_message_method).)|  
  
## Inheritance Hierarchy  
 [message_processor](../vs140/message_processor-Class.md)  
  
 `ordered_message_processor`  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
##  <a name="ordered_message_processor__async_send_method"></a>  ordered_message_processor::async_send Method  
 Asynchronously queues up messages and starts a processing task, if this has not been done already.  
  
```  
virtual void async_send(  
   _Inout_opt_ message<_Type> *                 _Msg  
);  
```  
  
### Parameters  
 `_Msg`  
 A pointer to a message.  
  
##  <a name="ordered_message_processor__initialize_method"></a>  ordered_message_processor::initialize Method  
 Initializes the                 `ordered_message_processor` object with the appropriate callback function, scheduler and schedule group.  
  
```  
void initialize(  
   _Inout_opt_ Scheduler *                 _PScheduler,  
   _Inout_opt_ ScheduleGroup *                 _PScheduleGroup,  
   _Handler_method const&                 _Handler  
);  
```  
  
### Parameters  
 `_PScheduler`  
 A pointer to the scheduler to be used for scheduling light-weight tasks.  
  
 `_PScheduleGroup`  
 A pointer to the schedule group to be used for scheduling light-weight tasks.  
  
 `_Handler`  
 The handler functor invoked during callback.  
  
##  <a name="ordered_message_processor__initialize_batched_processing_method"></a>  ordered_message_processor::initialize_batched_processing Method  
 Initialize batched message processing  
  
```  
virtual void initialize_batched_processing(  
   _Handler_method const&                 _Processor,  
   _Propagator_method const&                 _Propagator  
);  
```  
  
### Parameters  
 `_Processor`  
 The processor functor invoked during callback.  
  
 `_Propagator`  
 The propagator functor invoked during callback.  
  
##  <a name="ordered_message_processor__ordered_message_processor_constructor"></a>  ordered_message_processor::ordered_message_processor Constructor  
 Constructs an                 `ordered_message_processor` object.  
  
```  
ordered_message_processor();  
```  
  
### Remarks  
 This                         `ordered_message_processor` will not schedule asynchronous or synchronous handlers until the                         `initialize` function is called.  
  
##  <a name="ordered_message_processor___dtorordered_message_processor_destructor"></a>  ordered_message_processor::~ordered_message_processor Destructor  
 Destroys the                 `ordered_message_processor` object.  
  
```  
virtual ~ordered_message_processor();  
```  
  
### Remarks  
 Waits for all outstanding asynchronous operations before destroying the processor.  
  
##  <a name="ordered_message_processor__process_incoming_message_method"></a>  ordered_message_processor::process_incoming_message Method  
 The processing function that is called asynchronously. It dequeues messages and begins processing them.  
  
```  
virtual void process_incoming_message();  
```  
  
##  <a name="ordered_message_processor__sync_send_method"></a>  ordered_message_processor::sync_send Method  
 Synchronously queues up messages and starts a processing task, if this has not been done already.  
  
```  
virtual void sync_send(  
   _Inout_opt_ message<_Type> *                 _Msg  
);  
```  
  
### Parameters  
 `_Msg`  
 A pointer to a message.  
  
##  <a name="ordered_message_processor__wait_method"></a>  ordered_message_processor::wait Method  
 A processor-specific spin wait used in destructors of message blocks to make sure that all asynchronous processing tasks have time to finish before destroying the block.  
  
```  
virtual void wait();  
```  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)