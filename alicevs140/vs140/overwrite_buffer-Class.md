---
title: "overwrite_buffer Class"
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
ms.assetid: 5cc428fe-3697-419c-9fb2-78f6181c9293
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# overwrite_buffer Class
An             `overwrite_buffer` messaging block is a multi-target, multi-source, ordered             `propagator_block` capable of storing a single message at a time. New messages overwrite previously held ones.  
  
## Syntax  
  
```  
template<  
   class             _Type  
>  
class overwrite_buffer : public propagator_block<multi_link_registry<ITarget<            _Type>>, multi_link_registry<ISource<            _Type>>>;  
```  
  
#### Parameters  
 `_Type`  
 The payload type of the messages stored and propagated by the buffer.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[overwrite_buffer::overwrite_buffer Constructor](#overwrite_buffer__overwrite_buffer_constructor)|Overloaded. Constructs an                                         `overwrite_buffer` messaging block.|  
|[overwrite_buffer::~overwrite_buffer Destructor](#overwrite_buffer___dtoroverwrite_buffer_destructor)|Destroys the                                         `overwrite_buffer` messaging block.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[overwrite_buffer::has_value Method](#overwrite_buffer__has_value_method)|Checks whether this                                         `overwrite_buffer` messaging block has a value yet.|  
|[overwrite_buffer::value Method](#overwrite_buffer__value_method)|Gets a reference to the current payload of the message being stored in the                                         `overwrite_buffer` messaging block.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[overwrite_buffer::accept_message Method](#overwrite_buffer__accept_message_method)|Accepts a message that was offered by this                                         `overwrite_buffer` messaging block, returning a copy of the message to the caller.|  
|[overwrite_buffer::consume_message Method](#overwrite_buffer__consume_message_method)|Consumes a message previously offered by the                                         `overwrite_buffer` messaging block and reserved by the target, returning a copy of the message to the caller.|  
|[overwrite_buffer::link_target_notification Method](#overwrite_buffer__link_target_notification_method)|A callback that notifies that a new target has been linked to this                                         `overwrite_buffer` messaging block.|  
|[overwrite_buffer::propagate_message Method](#overwrite_buffer__propagate_message_method)|Asynchronously passes a message from an                                         `ISource` block to this                                         `overwrite_buffer` messaging block. It is invoked by the                                         `propagate` method, when called by a source block.|  
|[overwrite_buffer::propagate_to_any_targets Method](#overwrite_buffer__propagate_to_any_targets_method)|Places the                                         `message``_PMessage` in this                                         `overwrite_buffer` messaging block and offers it to all of the linked targets.|  
|[overwrite_buffer::release_message Method](#overwrite_buffer__release_message_method)|Releases a previous message reservation. (Overrides                                         [source_block::release_message](../vs140/source_block-Class.md#source_block__release_message_method).)|  
|[overwrite_buffer::reserve_message Method](#overwrite_buffer__reserve_message_method)|Reserves a message previously offered by this                                         `overwrite_buffer` messaging block. (Overrides                                         [source_block::reserve_message](../vs140/source_block-Class.md#source_block__reserve_message_method).)|  
|[overwrite_buffer::resume_propagation Method](#overwrite_buffer__resume_propagation_method)|Resumes propagation after a reservation has been released. (Overrides                                         [source_block::resume_propagation](../vs140/source_block-Class.md#source_block__resume_propagation_method).)|  
|[overwrite_buffer::send_message Method](#overwrite_buffer__send_message_method)|Synchronously passes a message from an                                         `ISource` block to this                                         `overwrite_buffer` messaging block. It is invoked by the                                         `send` method, when called by a source block.|  
|[overwrite_buffer::supports_anonymous_source Method](#overwrite_buffer__supports_anonymous_source_method)|Overrides the                                         `supports_anonymous_source` method to indicate that this block can accept messages offered to it by a source that is not linked. (Overrides                                         [ITarget::supports_anonymous_source](../vs140/ITarget-Class.md#itarget__supports_anonymous_source_method).)|  
  
## Remarks  
 An                 `overwrite_buffer` messaging block propagates out copies of its stored message to each of its targets.  
  
 For more information, see                 [Asynchronous Message Blocks](../vs140/Asynchronous-Message-Blocks.md).  
  
## Inheritance Hierarchy  
 [ISource](../vs140/ISource-Class.md)  
  
 [ITarget](../vs140/ITarget-Class.md)  
  
 [source_block](../vs140/source_block-Class.md)  
  
 [propagator_block](../vs140/propagator_block-Class.md)  
  
 `overwrite_buffer`  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
##  <a name="overwrite_buffer__accept_message_method"></a>  overwrite_buffer::accept_message Method  
 Accepts a message that was offered by this                 `overwrite_buffer` messaging block, returning a copy of the message to the caller.  
  
```  
virtual message<_Type> * accept_message(  
   runtime_object_identity                 _MsgId  
);  
```  
  
### Parameters  
 `_MsgId`  
 The                                 `runtime_object_identity` of the offered                                 `message` object.  
  
### Return Value  
 A pointer to the                         `message` object that the caller now has ownership of.  
  
### Remarks  
 The                         `overwrite_buffer` messaging block returns copies of the message to its targets, rather than transferring ownership of the currently held message.  
  
##  <a name="overwrite_buffer__consume_message_method"></a>  overwrite_buffer::consume_message Method  
 Consumes a message previously offered by the                 `overwrite_buffer` messaging block and reserved by the target, returning a copy of the message to the caller.  
  
```  
virtual message<_Type> * consume_message(  
   runtime_object_identity                 _MsgId  
);  
```  
  
### Parameters  
 `_MsgId`  
 The                                 `runtime_object_identity` of the                                 `message` object being consumed.  
  
### Return Value  
 A pointer to the                         `message` object that the caller now has ownership of.  
  
### Remarks  
 Similar to                         `accept`, but is always preceded by a call to                         `reserve`.  
  
##  <a name="overwrite_buffer__has_value_method"></a>  overwrite_buffer::has_value Method  
 Checks whether this                 `overwrite_buffer` messaging block has a value yet.  
  
```  
bool has_value() const;  
```  
  
### Return Value  
 `true` if the block has received a value,                         `false` otherwise.  
  
##  <a name="overwrite_buffer__link_target_notification_method"></a>  overwrite_buffer::link_target_notification Method  
 A callback that notifies that a new target has been linked to this                 `overwrite_buffer` messaging block.  
  
```  
virtual void link_target_notification(  
   _Inout_ ITarget<_Type> *                 _PTarget  
);  
```  
  
### Parameters  
 `_PTarget`  
 A pointer to the newly linked target.  
  
##  <a name="overwrite_buffer___dtoroverwrite_buffer_destructor"></a>  overwrite_buffer::~overwrite_buffer Destructor  
 Destroys the                 `overwrite_buffer` messaging block.  
  
```  
~overwrite_buffer();  
```  
  
##  <a name="overwrite_buffer__overwrite_buffer_constructor"></a>  overwrite_buffer::overwrite_buffer Constructor  
 Constructs an                 `overwrite_buffer` messaging block.  
  
```  
overwrite_buffer();  
  
overwrite_buffer(  
   filter_method const&                 _Filter  
);  
  
overwrite_buffer(  
   Scheduler&                 _PScheduler  
);  
  
overwrite_buffer(  
   Scheduler&                 _PScheduler,  
   filter_method const&                 _Filter  
);  
  
overwrite_buffer(  
   ScheduleGroup&                 _PScheduleGroup  
);  
  
overwrite_buffer(  
   ScheduleGroup&                 _PScheduleGroup,  
   filter_method const&                 _Filter  
);  
```  
  
### Parameters  
 `_Filter`  
 A filter function which determines whether offered messages should be accepted.  
  
 `_PScheduler`  
 The                                 `Scheduler` object within which the propagation task for the                                 `overwrite_buffer` messaging block is scheduled.  
  
 `_PScheduleGroup`  
 The                                 `ScheduleGroup` object within which the propagation task for the                                 `overwrite_buffer` messaging block is scheduled. The                                 `Scheduler` object used is implied by the schedule group.  
  
### Remarks  
 The runtime uses the default scheduler if you do not specify the                         `_PScheduler` or                         `_PScheduleGroup` parameters.  
  
 The type                         `filter_method` is a functor with signature                         `bool (_Type const &)` which is invoked by this                         `overwrite_buffer` messaging block to determine whether or not it should accept an offered message.  
  
##  <a name="overwrite_buffer__propagate_message_method"></a>  overwrite_buffer::propagate_message Method  
 Asynchronously passes a message from an                 `ISource` block to this                 `overwrite_buffer` messaging block. It is invoked by the                 `propagate` method, when called by a source block.  
  
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
  
##  <a name="overwrite_buffer__propagate_to_any_targets_method"></a>  overwrite_buffer::propagate_to_any_targets Method  
 Places the                 `message``_PMessage` in this                 `overwrite_buffer` messaging block and offers it to all of the linked targets.  
  
```  
virtual void propagate_to_any_targets(  
   _Inout_ message<_Type> *                 _PMessage  
);  
```  
  
### Parameters  
 `_PMessage`  
 A pointer to a                                 `message` object that this                                 `overwrite_buffer` has taken ownership of.  
  
### Remarks  
 This method overwrites the current message in the                         `overwrite_buffer` with the newly accepted message                         `_PMessage`.  
  
##  <a name="overwrite_buffer__send_message_method"></a>  overwrite_buffer::send_message Method  
 Synchronously passes a message from an                 `ISource` block to this                 `overwrite_buffer` messaging block. It is invoked by the                 `send` method, when called by a source block.  
  
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
  
##  <a name="overwrite_buffer__supports_anonymous_source_method"></a>  overwrite_buffer::supports_anonymous_source Method  
 Overrides the                 `supports_anonymous_source` method to indicate that this block can accept messages offered to it by a source that is not linked.  
  
```  
virtual bool supports_anonymous_source();  
```  
  
### Return Value  
 `true` because the block does not postpone offered messages.  
  
##  <a name="overwrite_buffer__release_message_method"></a>  overwrite_buffer::release_message Method  
 Releases a previous message reservation.  
  
```  
virtual void release_message(  
   runtime_object_identity                 _MsgId  
);  
```  
  
### Parameters  
 `_MsgId`  
 The                                 `runtime_object_identity` of the                                 `message` object being released.  
  
##  <a name="overwrite_buffer__reserve_message_method"></a>  overwrite_buffer::reserve_message Method  
 Reserves a message previously offered by this                 `overwrite_buffer` messaging block.  
  
```  
virtual bool reserve_message(  
   runtime_object_identity                 _MsgId  
);  
```  
  
### Parameters  
 `_MsgId`  
 The                                 `runtime_object_identity` of the                                 `message` object being reserved.  
  
### Return Value  
 `true` if the message was successfully reserved,                         `false` otherwise.  
  
### Remarks  
 After                         `reserve` is called, if it returns                         `true`, either                         `consume` or                         `release` must be called to either take or release ownership of the message.  
  
##  <a name="overwrite_buffer__resume_propagation_method"></a>  overwrite_buffer::resume_propagation Method  
 Resumes propagation after a reservation has been released.  
  
```  
virtual void resume_propagation();  
```  
  
##  <a name="overwrite_buffer__value_method"></a>  overwrite_buffer::value Method  
 Gets a reference to the current payload of the message being stored in the                 `overwrite_buffer` messaging block.  
  
```  
_Type value();  
```  
  
### Return Value  
 The payload of the currently stored message.  
  
### Remarks  
 The value stored in the                         `overwrite_buffer` could change immediately after this method returns. This method will wait until a message arrives if no message is currently stored in the                         `overwrite_buffer`.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [unbounded_buffer Class](../vs140/unbounded_buffer-Class.md)   
 [single_assignment Class](../vs140/single_assignment-Class.md)