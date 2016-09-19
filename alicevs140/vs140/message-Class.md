---
title: "message Class"
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
ms.assetid: 3e1f3505-6c0c-486c-8191-666d0880ec62
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# message Class
The basic message envelope containing the data payload being passed between messaging blocks.  
  
## Syntax  
  
```  
template<  
   class             _Type  
>  
class message : public ::Concurrency::details::_Runtime_object;  
```  
  
#### Parameters  
 `_Type`  
 The data type of the payload within the message.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`type`|A type alias for                                         `_Type`.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[message::message Constructor](#message__message_constructor)|Overloaded. Constructs a                                         `message` object.|  
|[message::~message Destructor](#message___dtormessage_destructor)|Destroys the                                         `message` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[message::add_ref Method](#message__add_ref_method)|Adds to the reference count for the                                         `message` object. Used for message blocks that need reference counting to determine message lifetimes.|  
|[message::msg_id Method](#message__msg_id_method)|Returns the ID of the                                         `message` object.|  
|[message::remove_ref Method](#message__remove_ref_method)|Subtracts from the reference count for the                                         `message` object. Used for message blocks that need reference counting to determine message lifetimes.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[message::payload Data Member](#message__payload_data_member)|The payload of the                                         `message` object.|  
  
## Remarks  
 For more information, see                 [Asynchronous Message Blocks](../vs140/Asynchronous-Message-Blocks.md).  
  
## Inheritance Hierarchy  
 `message`  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
##  <a name="message__add_ref_method"></a>  message::add_ref Method  
 Adds to the reference count for the                 `message` object. Used for message blocks that need reference counting to determine message lifetimes.  
  
```  
long add_ref();  
```  
  
### Return Value  
 The new value of the reference count.  
  
##  <a name="message__message_constructor"></a>  message::message Constructor  
 Constructs a                 `message` object.  
  
```  
message(  
   _Type const &                _P  
);  
  
message(  
   _Type const &                _P,  
   runtime_object_identity                 _Id  
);  
  
message(  
   message const &                 _Msg  
);  
  
message(  
   _In_ message const *                 _Msg  
);  
```  
  
### Parameters  
 `_P`  
 The payload of this message.  
  
 `_Id`  
 The unique ID of this message.  
  
 `_Msg`  
 A reference or pointer to a                                 `message` object.  
  
### Remarks  
 The constructor that takes a pointer to a                         `message` object as an argument throws an                         [invalid_argument](../vs140/invalid_argument-Class.md) exception if the parameter                         `_Msg` is                         `NULL`.  
  
##  <a name="message___dtormessage_destructor"></a>  message::~message Destructor  
 Destroys the                 `message` object.  
  
```  
virtual ~message();  
```  
  
##  <a name="message__msg_id_method"></a>  message::msg_id Method  
 Returns the ID of the                 `message` object.  
  
```  
runtime_object_identity msg_id() const;  
```  
  
### Return Value  
 The                         `runtime_object_identity` of the                         `message` object.  
  
##  <a name="message__payload_data_member"></a>  message::payload Data Member  
 The payload of the                 `message` object.  
  
```  
_Type const payload;  
```  
  
##  <a name="message__remove_ref_method"></a>  message::remove_ref Method  
 Subtracts from the reference count for the                 `message` object. Used for message blocks that need reference counting to determine message lifetimes.  
  
```  
long remove_ref();  
```  
  
### Return Value  
 The new value of the reference count.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)