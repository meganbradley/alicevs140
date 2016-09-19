---
title: "single_link_registry Class"
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
ms.assetid: 09540a4e-c34e-4ff9-af49-21b8612b6ab3
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# single_link_registry Class
The             `single_link_registry` object is a             `network_link_registry` that manages only a single source or target block.  
  
## Syntax  
  
```  
template<  
   class             _Block  
>  
class single_link_registry : public network_link_registry<            _Block>;  
```  
  
#### Parameters  
 `_Block`  
 The block data type being stored in the                         `single_link_registry` object.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[single_link_registry::single_link_registry Constructor](#single_link_registry__single_link_registry_constructor)|Constructs a                                         `single_link_registry` object.|  
|[single_link_registry::~single_link_registry Destructor](#single_link_registry___dtorsingle_link_registry_destructor)|Destroys the                                         `single_link_registry` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[single_link_registry::add Method](#single_link_registry__add_method)|Adds a link to the                                         `single_link_registry` object. (Overrides                                         [network_link_registry::add](../vs140/network_link_registry-Class.md#network_link_registry__add_method).)|  
|[single_link_registry::begin Method](#single_link_registry__begin_method)|Returns an iterator to the first element in the                                         `single_link_registry` object. (Overrides                                         [network_link_registry::begin](../vs140/network_link_registry-Class.md#network_link_registry__begin_method).)|  
|[single_link_registry::contains Method](#single_link_registry__contains_method)|Searches the                                         `single_link_registry` object for a specified block. (Overrides                                         [network_link_registry::contains](../vs140/network_link_registry-Class.md#network_link_registry__contains_method).)|  
|[single_link_registry::count Method](#single_link_registry__count_method)|Counts the number of items in the                                         `single_link_registry` object. (Overrides                                         [network_link_registry::count](../vs140/network_link_registry-Class.md#network_link_registry__count_method).)|  
|[single_link_registry::remove Method](#single_link_registry__remove_method)|Removes a link from the                                         `single_link_registry` object. (Overrides                                         [network_link_registry::remove](../vs140/network_link_registry-Class.md#network_link_registry__remove_method).)|  
  
## Inheritance Hierarchy  
 [network_link_registry](../vs140/network_link_registry-Class.md)  
  
 `single_link_registry`  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
##  <a name="single_link_registry__add_method"></a>  single_link_registry::add Method  
 Adds a link to the                 `single_link_registry` object.  
  
```  
virtual void add(  
   _EType                 _Link  
);  
```  
  
### Parameters  
 `_Link`  
 A pointer to a block to be added.  
  
### Remarks  
 The method throws an                         [invalid_link_target](../vs140/invalid_link_target-Class.md) exception if there is already a link in this registry.  
  
##  <a name="single_link_registry__begin_method"></a>  single_link_registry::begin Method  
 Returns an iterator to the first element in the                 `single_link_registry` object.  
  
```  
virtual iterator begin();  
```  
  
### Return Value  
 An iterator addressing the first element in the                         `single_link_registry` object.  
  
### Remarks  
 The end state is indicated by a                         `NULL` link.  
  
##  <a name="single_link_registry__contains_method"></a>  single_link_registry::contains Method  
 Searches the                 `single_link_registry` object for a specified block.  
  
```  
virtual bool contains(  
   _EType                 _Link  
);  
```  
  
### Parameters  
 `_Link`  
 A pointer to a block that is to be searched for in the                                 `single_link_registry` object.  
  
### Return Value  
 `true` if the link was found,                         `false` otherwise.  
  
##  <a name="single_link_registry__count_method"></a>  single_link_registry::count Method  
 Counts the number of items in the                 `single_link_registry` object.  
  
```  
virtual size_t count();  
```  
  
### Return Value  
 The number of items in the                         `single_link_registry` object.  
  
##  <a name="single_link_registry__remove_method"></a>  single_link_registry::remove Method  
 Removes a link from the                 `single_link_registry` object.  
  
```  
virtual bool remove(  
   _EType                 _Link  
);  
```  
  
### Parameters  
 `_Link`  
 A pointer to a block to be removed, if found.  
  
### Return Value  
 `true` if the link was found and removed,                         `false` otherwise.  
  
##  <a name="single_link_registry__single_link_registry_constructor"></a>  single_link_registry::single_link_registry Constructor  
 Constructs a                 `single_link_registry` object.  
  
```  
single_link_registry();  
```  
  
##  <a name="single_link_registry___dtorsingle_link_registry_destructor"></a>  single_link_registry::~single_link_registry Destructor  
 Destroys the                 `single_link_registry` object.  
  
```  
virtual ~single_link_registry();  
```  
  
### Remarks  
 The method throws an                         [invalid_operation](../vs140/invalid_operation-Class.md) exception if it is called before the link is removed.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [multi_link_registry Class](../vs140/multi_link_registry-Class.md)