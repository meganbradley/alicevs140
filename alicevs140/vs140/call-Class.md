---
title: "call Class"
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
ms.assetid: 1521970a-1e9c-4b0c-a681-d18e40976f49
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# call Class
A             `call` messaging block is a multi-source, ordered             `target_block` that invokes a specified function when receiving a message.  
  
## Syntax  
  
```  
template<  
   class             _Type,  
   class             _FunctorType = std::tr1::function<void(_Type const&)>  
>  
class call : public target_block<multi_link_registry<ISource<            _Type>>>;  
```  
  
#### Parameters  
 `_Type`  
 The payload type of the messages propagated to this block.  
  
 `_FunctorType`  
 The signature of functions that this block can accept.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[call::call Constructor](#call__call_constructor)|Overloaded. Constructs a                                         `call` messaging block.|  
|[call::~call Destructor](#call___dtorcall_destructor)|Destroys the                                         `call` messaging block.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[call::process_input_messages Method](#call__process_input_messages_method)|Executes the call function on the input messages.|  
|[call::process_message Method](#call__process_message_method)|Processes a message that was accepted by this                                         `call` messaging block.|  
|[call::propagate_message Method](#call__propagate_message_method)|Asynchronously passes a message from an                                         `ISource` block to this                                         `call` messaging block. It is invoked by the                                         `propagate` method, when called by a source block.|  
|[call::send_message Method](#call__send_message_method)|Synchronously passes a message from an                                         `ISource` block to this                                         `call` messaging block. It is invoked by the                                         `send` method, when called by a source block.|  
|[call::supports_anonymous_source Method](#call__supports_anonymous_source_method)|Overrides the                                         `supports_anonymous_source` method to indicate that this block can accept messages offered to it by a source that is not linked. (Overrides                                         [ITarget::supports_anonymous_source](../vs140/ITarget-Class.md#itarget__supports_anonymous_source_method).)|  
  
## Remarks  
 For more information, see                 [Asynchronous Message Blocks](../vs140/Asynchronous-Message-Blocks.md).  
  
## Inheritance Hierarchy  
 [ITarget](../vs140/ITarget-Class.md)  
  
 [target_block](../vs140/target_block-Class.md)  
  
 `call`  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
##  <a name="call__call_constructor"></a>  call::call Constructor  
 Constructs a                 `call` messaging block.  
  
```  
call(  
   _Call_method const&                 _Func  
);  
  
call(  
   _Call_method const&                 _Func,  
   filter_method const&                 _Filter  
);  
  
call(  
   Scheduler&                 _PScheduler,  
   _Call_method const&                 _Func  
);  
  
call(  
   Scheduler&                 _PScheduler,  
   _Call_method const&                 _Func,  
   filter_method const&                 _Filter  
);  
  
call(  
   ScheduleGroup&                 _PScheduleGroup,  
   _Call_method const&                 _Func  
);  
  
call(  
   ScheduleGroup&                 _PScheduleGroup,  
   _Call_method const&                 _Func,  
   filter_method const&                 _Filter  
);  
```  
  
### Parameters  
 `_Func`  
 A function that will be invoked for each accepted message.  
  
 `_Filter`  
 A filter function which determines whether offered messages should be accepted.  
  
 `_PScheduler`  
 The                                 `Scheduler` object within which the propagation task for the                                 `call` messaging block is scheduled.  
  
 `_PScheduleGroup`  
 The                                 `ScheduleGroup` object within which the propagation task for the                                 `call` messaging block is scheduled. The                                 `Scheduler` object used is implied by the schedule group.  
  
### Remarks  
 The runtime uses the default scheduler if you do not specify the                         `_PScheduler` or                         `_PScheduleGroup` parameters.  
  
 The type                         `_Call_method` is a functor with signature                         `void (_Type const &)` which is invoked by this                         `call` messaging block to process a message.  
  
 The type                         `filter_method` is a functor with signature                         `bool (_Type const &)` which is invoked by this                         `call` messaging block to determine whether or not it should accept an offered message.  
  
##  <a name="call___dtorcall_destructor"></a>  call::~call Destructor  
 Destroys the                 `call` messaging block.  
  
```  
~call();  
```  
  
##  <a name="call__process_input_messages_method"></a>  call::process_input_messages Method  
 Executes the call function on the input messages.  
  
```  
virtual void process_input_messages(  
   _Inout_ message<_Type> *                 _PMessage  
);  
```  
  
### Parameters  
 `_PMessage`  
  
##  <a name="call__process_message_method"></a>  call::process_message Method  
 Processes a message that was accepted by this                 `call` messaging block.  
  
```  
virtual void process_message(  
   _Inout_ message<_Type> *                 _PMessage  
);  
```  
  
### Parameters  
 `_PMessage`  
 A pointer to the message that is to be handled.  
  
##  <a name="call__propagate_message_method"></a>  call::propagate_message Method  
 Asynchronously passes a message from an                 `ISource` block to this                 `call` messaging block. It is invoked by the                 `propagate` method, when called by a source block.  
  
```  
virtual message_status propagate_message(  
   _Inout_ message<_Type> *                 _PMessage,  
   _Inout_ ISource<_Type> *                 _PSource  
);  
```  
  
### Parameters  
 `_PMessage`  
 A pointer to the                                 `message` object.  
  
 `_PSource`  
 A pointer to the source block offering the message.  
  
### Return Value  
 A                         [message_status](concurrency_namespace_Enumerations) indication of what the target decided to do with the message.  
  
##  <a name="call__send_message_method"></a>  call::send_message Method  
 Synchronously passes a message from an                 `ISource` block to this                 `call` messaging block. It is invoked by the                 `send` method, when called by a source block.  
  
```  
virtual message_status send_message(  
   _Inout_ message<_Type> *                 _PMessage,  
   _Inout_ ISource<_Type> *                 _PSource  
);  
```  
  
### Parameters  
 `_PMessage`  
 A pointer to the                                 `message` object.  
  
 `_PSource`  
 A pointer to the source block offering the message.  
  
### Return Value  
 A                         [message_status](concurrency_namespace_Enumerations) indication of what the target decided to do with the message.  
  
##  <a name="call__supports_anonymous_source_method"></a>  call::supports_anonymous_source Method  
 Overrides the                 `supports_anonymous_source` method to indicate that this block can accept messages offered to it by a source that is not linked.  
  
```  
virtual bool supports_anonymous_source();  
```  
  
### Return Value  
 `true` because the block does not postpone offered messages.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [transformer Class](../vs140/transformer-Class.md)