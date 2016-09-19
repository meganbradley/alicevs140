---
title: "ITopologyNode Structure"
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
ms.assetid: 92e7e032-04f6-4c7c-be36-8f9a35fc4734
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITopologyNode Structure
An interface to a topology node as defined by the Resource Manager. A node contains one or more execution resources.  
  
## Syntax  
  
```  
struct ITopologyNode;  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[ITopologyNode::GetExecutionResourceCount Method](#itopologynode__getexecutionresourcecount_method)|Returns the number of execution resources grouped together under this node.|  
|[ITopologyNode::GetFirstExecutionResource Method](#itopologynode__getfirstexecutionresource_method)|Returns the first execution resource grouped under this node in enumeration order.|  
|[ITopologyNode::GetId Method](#itopologynode__getid_method)|Returns the Resource Manager's unique identifier for this node.|  
|[ITopologyNode::GetNext Method](#itopologynode__getnext_method)|Returns an interface to the next topology node in enumeration order.|  
|[ITopologyNode::GetNumaNode Method](#itopologynode__getnumanode_method)|Returns the Windows assigned NUMA node number to which this Resource Maanger node belongs.|  
  
## Remarks  
 This interface is typically utilized to walk the topology of the system as observed by the Resource Manager.  
  
## Inheritance Hierarchy  
 `ITopologyNode`  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
##  <a name="itopologynode__getexecutionresourcecount_method"></a>  ITopologyNode::GetExecutionResourceCount Method  
 Returns the number of execution resources grouped together under this node.  
  
```  
virtual unsigned int GetExecutionResourceCount() const =0;  
```  
  
### Return Value  
 The number of execution resources grouped together under this node.  
  
##  <a name="itopologynode__getfirstexecutionresource_method"></a>  ITopologyNode::GetFirstExecutionResource Method  
 Returns the first execution resource grouped under this node in enumeration order.  
  
```  
virtual ITopologyExecutionResource *GetFirstExecutionResource() const =0;  
```  
  
### Return Value  
 The first execution resource grouped under this node in enumeration order.  
  
##  <a name="itopologynode__getid_method"></a>  ITopologyNode::GetId Method  
 Returns the Resource Manager's unique identifier for this node.  
  
```  
virtual unsigned int GetId() const =0;  
```  
  
### Return Value  
 The Resource Manager's unique identifier for this node.  
  
### Remarks  
 The Concurrency Runtime represents hardware threads on the system in groups of processor nodes. Nodes are usually derived from the hardware topology of the system. For example, all processors on a specific socket or a specific NUMA node may belong to the same processor node. The Resource Manager assigns unique identifiers to these nodes starting with                         `0` up to and including                         `nodeCount - 1`, where                         `nodeCount` represents the total number of processor nodes on the system.  
  
 The count of nodes can be obtained from the function                         [GetProcessorNodeCount](concurrency_namespace_Functions).  
  
##  <a name="itopologynode__getnext_method"></a>  ITopologyNode::GetNext Method  
 Returns an interface to the next topology node in enumeration order.  
  
```  
virtual ITopologyNode *GetNext() const =0;  
```  
  
### Return Value  
 An interface to the next node in enumeration order. If there are no more nodes in enumeration order of the system topology, this method will return the value                         `NULL`.  
  
##  <a name="itopologynode__getnumanode_method"></a>  ITopologyNode::GetNumaNode Method  
 Returns the Windows assigned NUMA node number to which this Resource Maanger node belongs.  
  
```  
virtual unsigned long GetNumaNode() const =0;  
```  
  
### Return Value  
 The Windows assigned NUMA node number to which this Resource Manager node belongs.  
  
### Remarks  
 A thread proxy running on a virtual processor root belonging to this node will have affinity to at least the NUMA node level for the NUMA node returned by this method.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)