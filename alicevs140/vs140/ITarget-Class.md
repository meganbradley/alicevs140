---
title: "ITarget Class"
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
ms.assetid: 5678db25-112a-4f72-be13-42e16b67c48b
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITarget Class
The             `ITarget` class is the interface for all target blocks. Target blocks consume messages offered to them by             `ISource` blocks.  
  
## Syntax  
  
```  
template<  
   class             _Type  
>  
class ITarget;  
```  
  
#### Parameters  
 `_Type`  
 The data type of the payload within the messages accepted by the target block.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`filter_method`|The signature of any method used by the block that returns a                                         `bool` value to determine whether an offered message should be accepted.|  
|`type`|A type alias for                                         `_Type`.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[ITarget::~ITarget Destructor](#itarget___dtoritarget_destructor)|Destroys the                                         `ITarget` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ITarget::propagate Method](#itarget__propagate_method)|When overridden in a derived class, asynchronously passes a message from a source block to this target block.|  
|[ITarget::send Method](#itarget__send_method)|When overridden in a derived class, synchronously passes a message to the target block.|  
|[ITarget::supports_anonymous_source Method](#itarget__supports_anonymous_source_method)|When overridden in a derived class, returns true or false depending on whether the message block accepts messages offered by a source that is not linked to it. If the overridden method returns                                         `true`, the target cannot postpone an offered message, as consumption of a postponed message at a later time requires the source to be identified in its sourse link registry.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ITarget::link_source Method](#itarget__link_source_method)|When overridden in a derived class, links a specified source block to this                                         `ITarget` block.|  
|[ITarget::unlink_source Method](#itarget__unlink_source_method)|When overridden in a derived class, unlinks a specified source block from this                                         `ITarget` block.|  
|[ITarget::unlink_sources Method](#itarget__unlink_sources_method)|When overridden in a derived class, unlinks all source blocks from this                                         `ITarget` block.|  
  
## Remarks  
 For more information, see                 [Asynchronous Message Blocks](../vs140/Asynchronous-Message-Blocks.md).  
  
## Inheritance Hierarchy  
 `ITarget`  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
##  <a name="itarget___dtoritarget_destructor"></a>  ITarget::~ITarget Destructor  
 Destroys the                 `ITarget` object.  
  
```  
virtual ~ITarget();  
```  
  
##  <a name="itarget__link_source_method"></a>  ITarget::link_source Method  
 When overridden in a derived class, links a specified source block to this                 `ITarget` block.  
  
```  
virtual void link_source(  
   _Inout_ ISource<_Type> *                 _PSource  
) = 0;  
```  
  
### Parameters  
 `_PSource`  
 The                                 `ISource` block being linked to this                                 `ITarget` block.  
  
### Remarks  
 This function should not be called directly on an                         `ITarget` block. Blocks should be connected together using the                         `link_target` method on                         `ISource` blocks, which will invoke the                         `link_source` method on the corresponding target.  
  
##  <a name="itarget__propagate_method"></a>  ITarget::propagate Method  
 When overridden in a derived class, asynchronously passes a message from a source block to this target block.  
  
```  
virtual message_status propagate(  
   _Inout_opt_ message<_Type> *                 _PMessage,  
   _Inout_opt_ ISource<_Type> *                 _PSource  
) = 0;  
```  
  
### Parameters  
 `_PMessage`  
 A pointer to the                                 `message` object.  
  
 `_PSource`  
 A pointer to the source block offering the message.  
  
### Return Value  
 A                         [message_status](concurrency_namespace_Enumerations) indication of what the target decided to do with the message.  
  
### Remarks  
 The method throws an                         [invalid_argument](../vs140/invalid_argument-Class.md) exception if either the                         `_PMessage` or                         `_PSource` parameter is                         `NULL`.  
  
##  <a name="itarget__send_method"></a>  ITarget::send Method  
 When overridden in a derived class, synchronously passes a message to the target block.  
  
```  
virtual message_status send(  
   _Inout_ message<_Type> *                 _PMessage,  
   _Inout_ ISource<_Type> *                 _PSource  
) = 0;  
```  
  
### Parameters  
 `_PMessage`  
 A pointer to the                                 `message` object.  
  
 `_PSource`  
 A pointer to the source block offering the message.  
  
### Return Value  
 A                         [message_status](concurrency_namespace_Enumerations) indication of what the target decided to do with the message.  
  
### Remarks  
 The method throws an                         [invalid_argument](../vs140/invalid_argument-Class.md) exception if either the                         `_PMessage` or                         `_PSource` parameter is                         `NULL`.  
  
 Using the                         `send` method outside of message initiation and to propagate messages within a network is dangerous and can lead to deadlock.  
  
 When                         `send` returns, the message has either already been accepted, and transferred into the target block, or it has been declined by the target.  
  
##  <a name="itarget__supports_anonymous_source_method"></a>  ITarget::supports_anonymous_source Method  
 When overridden in a derived class, returns true or false depending on whether the message block accepts messages offered by a source that is not linked to it. If the overridden method returns                 `true`, the target cannot postpone an offered message, as consumption of a postponed message at a later time requires the source to be identified in its sourse link registry.  
  
```  
virtual bool supports_anonymous_source();  
```  
  
### Return Value  
 `true` if the block can accept message from a source that is not linked to it                         `false` otherwise.  
  
##  <a name="itarget__unlink_source_method"></a>  ITarget::unlink_source Method  
 When overridden in a derived class, unlinks a specified source block from this                 `ITarget` block.  
  
```  
virtual void unlink_source(  
   _Inout_ ISource<_Type> *                 _PSource  
) = 0;  
```  
  
### Parameters  
 `_PSource`  
 The                                 `ISource` block being unlinked from this                                 `ITarget` block.  
  
### Remarks  
 This function should not be called directly on an                         `ITarget` block. Blocks should be disconnected using the                         `unlink_target` or                         `unlink_targets` methods on                         `ISource` blocks, which will invoke the                         `unlink_source` method on the corresponding target.  
  
##  <a name="itarget__unlink_sources_method"></a>  ITarget::unlink_sources Method  
 When overridden in a derived class, unlinks all source blocks from this                 `ITarget` block.  
  
```  
virtual void unlink_sources() = 0;  
```  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [ISource Class](../vs140/ISource-Class.md)