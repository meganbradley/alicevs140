---
title: "unbounded_buffer Class"
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
ms.assetid: 6b1a939a-1819-4385-b1d8-708f83d4ec47
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unbounded_buffer Class
An             `unbounded_buffer` messaging block is a multi-target, multi-source, ordered             `propagator_block` capable of storing an unbounded number of messages.  
  
## Syntax  
  
```  
template<  
   class             _Type  
>  
class unbounded_buffer : public propagator_block<multi_link_registry<ITarget<            _Type>>, multi_link_registry<ISource<            _Type>>>;  
```  
  
#### Parameters  
 `_Type`  
 The payload type of the messages stored and propagated by the buffer.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[unbounded_buffer::unbounded_buffer Constructor](#unbounded_buffer__unbounded_buffer_constructor)|Overloaded. Constructs an                                         `unbounded_buffer` messaging block.|  
|[unbounded_buffer::~unbounded_buffer Destructor](#unbounded_buffer___dtorunbounded_buffer_destructor)|Destroys the                                         `unbounded_buffer` messaging block.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[unbounded_buffer::dequeue Method](#unbounded_buffer__dequeue_method)|Removes an item from the                                         `unbounded_buffer` messaging block.|  
|[unbounded_buffer::enqueue Method](#unbounded_buffer__enqueue_method)|Adds an item to the                                         `unbounded_buffer` messaging block.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[unbounded_buffer::accept_message Method](#unbounded_buffer__accept_message_method)|Accepts a message that was offered by this                                         `unbounded_buffer` messaging block, transferring ownership to the caller.|  
|[unbounded_buffer::consume_message Method](#unbounded_buffer__consume_message_method)|Consumes a message previously offered by the                                         `unbounded_buffer` messaging block and reserved by the target, transferring ownership to the caller.|  
|[unbounded_buffer::link_target_notification Method](#unbounded_buffer__link_target_notification_method)|A callback that notifies that a new target has been linked to this                                         `unbounded_buffer` messaging block.|  
|[unbounded_buffer::process_input_messages Method](#unbounded_buffer__process_input_messages_method)|Places the                                         `message``_PMessage` in this                                         `unbounded_buffer` messaging block and tries to offer it to all of the linked targets.|  
|[unbounded_buffer::propagate_message Method](#unbounded_buffer__propagate_message_method)|Asynchronously passes a message from an                                         `ISource` block to this                                         `unbounded_buffer` messaging block. It is invoked by the                                         `propagate` method, when called by a source block.|  
|[unbounded_buffer::propagate_output_messages Method](#unbounded_buffer__propagate_output_messages_method)|Places the                                         `message``_PMessage` in this                                         `unbounded_buffer` messaging block and tries to offer it to all of the linked targets. (Overrides                                         [source_block::propagate_output_messages](../vs140/source_block-Class.md#source_block__propagate_output_messages_method).)|  
|[unbounded_buffer::release_message Method](#unbounded_buffer__release_message_method)|Releases a previous message reservation. (Overrides                                         [source_block::release_message](../vs140/source_block-Class.md#source_block__release_message_method).)|  
|[unbounded_buffer::reserve_message Method](#unbounded_buffer__reserve_message_method)|Reserves a message previously offered by this                                         `unbounded_buffer` messaging block. (Overrides                                         [source_block::reserve_message](../vs140/source_block-Class.md#source_block__reserve_message_method).)|  
|[unbounded_buffer::resume_propagation Method](#unbounded_buffer__resume_propagation_method)|Resumes propagation after a reservation has been released. (Overrides                                         [source_block::resume_propagation](../vs140/source_block-Class.md#source_block__resume_propagation_method).)|  
|[unbounded_buffer::send_message Method](#unbounded_buffer__send_message_method)|Synchronously passes a message from an                                         `ISource` block to this                                         `unbounded_buffer` messaging block. It is invoked by the                                         `send` method, when called by a source block.|  
|[unbounded_buffer::supports_anonymous_source Method](#unbounded_buffer__supports_anonymous_source_method)|Overrides the                                         `supports_anonymous_source` method to indicate that this block can accept messages offered to it by a source that is not linked. (Overrides                                         [ITarget::supports_anonymous_source](../vs140/ITarget-Class.md#itarget__supports_anonymous_source_method).)|  
  
## Remarks  
 For more information, see                 [Asynchronous Message Blocks](../vs140/Asynchronous-Message-Blocks.md).  
  
## Inheritance Hierarchy  
 [ISource](../vs140/ISource-Class.md)  
  
 [ITarget](../vs140/ITarget-Class.md)  
  
 [source_block](../vs140/source_block-Class.md)  
  
 [propagator_block](../vs140/propagator_block-Class.md)  
  
 `unbounded_buffer`  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
##  <a name="unbounded_buffer__accept_message_method"></a>  unbounded_buffer::accept_message Method  
 Accepts a message that was offered by this                 `unbounded_buffer` messaging block, transferring ownership to the caller.  
  
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
  
##  <a name="unbounded_buffer__consume_message_method"></a>  unbounded_buffer::consume_message Method  
 Consumes a message previously offered by the                 `unbounded_buffer` messaging block and reserved by the target, transferring ownership to the caller.  
  
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
  
##  <a name="unbounded_buffer__dequeue_method"></a>  unbounded_buffer::dequeue Method  
 Removes an item from the                 `unbounded_buffer` messaging block.  
  
```  
_Type dequeue();  
```  
  
### Return Value  
 The payload of the message removed from the                         `unbounded_buffer`.  
  
##  <a name="unbounded_buffer__enqueue_method"></a>  unbounded_buffer::enqueue Method  
 Adds an item to the                 `unbounded_buffer` messaging block.  
  
```  
bool enqueue(  
   _Type const&                 _Item  
);  
```  
  
### Parameters  
 `_Item`  
 The item to add.  
  
### Return Value  
 `true` if the item was accepted,                         `false` otherwise.  
  
##  <a name="unbounded_buffer__link_target_notification_method"></a>  unbounded_buffer::link_target_notification Method  
 A callback that notifies that a new target has been linked to this                 `unbounded_buffer` messaging block.  
  
```  
virtual void link_target_notification(  
   _Inout_ ITarget<_Type> *                 _PTarget  
);  
```  
  
### Parameters  
 `_PTarget`  
 A pointer to the newly linked target.  
  
##  <a name="unbounded_buffer__propagate_message_method"></a>  unbounded_buffer::propagate_message Method  
 Asynchronously passes a message from an                 `ISource` block to this                 `unbounded_buffer` messaging block. It is invoked by the                 `propagate` method, when called by a source block.  
  
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
  
##  <a name="unbounded_buffer__propagate_output_messages_method"></a>  unbounded_buffer::propagate_output_messages Method  
 Places the                 `message``_PMessage` in this                 `unbounded_buffer` messaging block and tries to offer it to all of the linked targets.  
  
```  
virtual void propagate_output_messages();  
```  
  
### Remarks  
 If another message is already ahead of this one in the                         `unbounded_buffer`, propagation to linked targets will not occur until any earlier messages have been accepted or consumed. The first linked target to successfully                         `accept` or                         `consume` the message takes ownership, and no other target can then get the message.  
  
##  <a name="unbounded_buffer__process_input_messages_method"></a>  unbounded_buffer::process_input_messages Method  
 Places the                 `message``_PMessage` in this                 `unbounded_buffer` messaging block and tries to offer it to all of the linked targets.  
  
```  
virtual void process_input_messages(  
   _Inout_ message<_Type> *                 _PMessage  
);  
```  
  
### Parameters  
 `_PMessage`  
  
##  <a name="unbounded_buffer__release_message_method"></a>  unbounded_buffer::release_message Method  
 Releases a previous message reservation.  
  
```  
virtual void release_message(  
   runtime_object_identity                 _MsgId  
);  
```  
  
### Parameters  
 `_MsgId`  
 The                                 `runtime_object_identity` of the                                 `message` object being released.  
  
##  <a name="unbounded_buffer__reserve_message_method"></a>  unbounded_buffer::reserve_message Method  
 Reserves a message previously offered by this                 `unbounded_buffer` messaging block.  
  
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
  
##  <a name="unbounded_buffer__resume_propagation_method"></a>  unbounded_buffer::resume_propagation Method  
 Resumes propagation after a reservation has been released.  
  
```  
virtual void resume_propagation();  
```  
  
##  <a name="unbounded_buffer__send_message_method"></a>  unbounded_buffer::send_message Method  
 Synchronously passes a message from an                 `ISource` block to this                 `unbounded_buffer` messaging block. It is invoked by the                 `send` method, when called by a source block.  
  
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
  
##  <a name="unbounded_buffer__supports_anonymous_source_method"></a>  unbounded_buffer::supports_anonymous_source Method  
 Overrides the                 `supports_anonymous_source` method to indicate that this block can accept messages offered to it by a source that is not linked.  
  
```  
virtual bool supports_anonymous_source();  
```  
  
### Return Value  
 `true` because the block does not postpone offered messages.  
  
##  <a name="unbounded_buffer__unbounded_buffer_constructor"></a>  unbounded_buffer::unbounded_buffer Constructor  
 Constructs an                 `unbounded_buffer` messaging block.  
  
```  
unbounded_buffer();  
  
unbounded_buffer(  
   filter_method const&                 _Filter  
);  
  
unbounded_buffer(  
   Scheduler&                 _PScheduler  
);  
  
unbounded_buffer(  
   Scheduler&                 _PScheduler,  
   filter_method const&                 _Filter  
);  
  
unbounded_buffer(  
   ScheduleGroup&                 _PScheduleGroup  
);  
  
unbounded_buffer(  
   ScheduleGroup&                 _PScheduleGroup,  
   filter_method const&                 _Filter  
);  
```  
  
### Parameters  
 `_Filter`  
 A filter function which determines whether offered messages should be accepted.  
  
 `_PScheduler`  
 The                                 `Scheduler` object within which the propagation task for the                                 `unbounded_buffer` messaging block is scheduled.  
  
 `_PScheduleGroup`  
 The                                 `ScheduleGroup` object within which the propagation task for the                                 `unbounded_buffer` messaging block is scheduled. The                                 `Scheduler` object used is implied by the schedule group.  
  
### Remarks  
 The runtime uses the default scheduler if you do not specify the                         `_PScheduler` or                         `_PScheduleGroup` parameters.  
  
 The type                         `filter_method` is a functor with signature                         `bool (_Type const &)` which is invoked by this                         `unbounded_buffer` messaging block to determine whether or not it should accept an offered message.  
  
##  <a name="unbounded_buffer___dtorunbounded_buffer_destructor"></a>  unbounded_buffer::~unbounded_buffer Destructor  
 Destroys the                 `unbounded_buffer` messaging block.  
  
```  
~unbounded_buffer();  
```  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [overwrite_buffer Class](../vs140/overwrite_buffer-Class.md)   
 [single_assignment Class](../vs140/single_assignment-Class.md)