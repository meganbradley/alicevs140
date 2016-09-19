---
title: "Scheduler Class"
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
ms.assetid: 34cf7961-048d-4852-8a5c-a32f823e3506
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Scheduler Class
Represents an abstraction for a Concurrency Runtime scheduler.  
  
## Syntax  
  
```  
class Scheduler;  
```  
  
## Members  
  
### Protected Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[Scheduler::Scheduler Constructor](#scheduler__scheduler_constructor)|An object of the                                         `Scheduler` class can only created using factory methods, or implicitly.|  
|[Scheduler::~Scheduler Destructor](#scheduler___dtorscheduler_destructor)|An object of the                                         `Scheduler` class is implicitly destroyed when all external references to it cease to exist.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[Scheduler::Attach Method](#scheduler__attach_method)|Attaches the scheduler to the calling context. After this method returns, the calling context is managed by the scheduler and the scheduler becomes the current scheduler.|  
|[Scheduler::Create Method](#scheduler__create_method)|Creates a new scheduler whose behavior is described by the                                         `_Policy` parameter, places an initial reference on the scheduler, and returns a pointer to it.|  
|[Scheduler::CreateScheduleGroup Method](#scheduler__createschedulegroup_method)|Overloaded. Creates a new schedule group within the scheduler. The version that takes the parameter                                         `_Placement` causes tasks within the newly created schedule group to be biased towards executing at the location specified by that parameter.|  
|[Scheduler::GetNumberOfVirtualProcessors Method](#scheduler__getnumberofvirtualprocessors_method)|Returns the current number of virtual processors for the scheduler.|  
|[Scheduler::GetPolicy Method](#scheduler__getpolicy_method)|Returns a copy of the policy that the scheduler was created with.|  
|[Scheduler::Id Method](#scheduler__id_method)|Returns a unique identifier for the scheduler.|  
|[Scheduler::IsAvailableLocation Method](#scheduler__isavailablelocation_method)|Determines whether a given location is available on the scheduler.|  
|[Scheduler::Reference Method](#scheduler__reference_method)|Increments the scheduler reference count.|  
|[Scheduler::RegisterShutdownEvent Method](#scheduler__registershutdownevent_method)|Causes the Windows event handle passed in the                                         `_Event` parameter to be signaled when the scheduler shuts down and destroys itself. At the time the event is signaled, all work that had been scheduled to the scheduler is complete. Multiple shutdown events can be registered through this method.|  
|[Scheduler::Release Method](#scheduler__release_method)|Decrements the scheduler reference count.|  
|[Scheduler::ResetDefaultSchedulerPolicy Method](#scheduler__resetdefaultschedulerpolicy_method)|Resets the default scheduler policy to the runtime default. The next time a default scheduler is created, it will use the runtime default policy settings.|  
|[Scheduler::ScheduleTask Method](#scheduler__scheduletask_method)|Overloaded. Schedules a light-weight task within the scheduler. The light-weight task will be placed in a schedule group determined by the runtime. The version that takes the parameter                                         `_Placement` causes the task to be biased towards executing at the specified location.|  
|[Scheduler::SetDefaultSchedulerPolicy Method](#scheduler__setdefaultschedulerpolicy_method)|Allows a user defined policy to be used to create the default scheduler. This method can be called only when no default scheduler exists within the process. After a default policy has been set, it remains in effect until the next valid call to either the                                         `SetDefaultSchedulerPolicy` or the                                         [ResetDefaultSchedulerPolicy](#scheduler__resetdefaultschedulerpolicy_method) method.|  
  
## Remarks  
 The Concurrency Runtime scheduler uses execution contexts, which map to the operating system execution contexts, such as a thread, to execute the work queued to it by your application. At any time, the concurrency level of a scheduler is equal to the number of virtual processor granted to it by the Resource Manager. A virtual processor is an abstraction for a processing resource and maps to a hardware thread on the underlying system. Only a single scheduler context can execute on a virtual processor at a given time.  
  
 The Concurrency Runtime will create a default scheduler per process to execute parallel work. In addition you can create your own scheduler instances and manipulate it using this class.  
  
## Inheritance Hierarchy  
 `Scheduler`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="scheduler__attach_method"></a>  Scheduler::Attach Method  
 Attaches the scheduler to the calling context. After this method returns, the calling context is managed by the scheduler and the scheduler becomes the current scheduler.  
  
```  
virtual void Attach() =0;  
```  
  
### Remarks  
 Attaching a scheduler implicitly places a reference on the scheduler.  
  
 At some point in the future, you must call the                         [CurrentScheduler::Detach](../vs140/CurrentScheduler-Class.md#currentscheduler__detach_method) method in order to allow the scheduler to shut down.  
  
 If this method is called from a context that is already attached to a different scheduler, the existing scheduler is remembered as the previous scheduler, and the newly created scheduler becomes the current scheduler. When you call the                         `CurrentScheduler::Detach` method at a later point, the previous scheduler is restored as the current scheduler.  
  
 This method will throw an                         [improper_scheduler_attach](../vs140/improper_scheduler_attach-Class.md) exception if this scheduler is the current scheduler of the calling context.  
  
##  <a name="scheduler__create_method"></a>  Scheduler::Create Method  
 Creates a new scheduler whose behavior is described by the                 `_Policy` parameter, places an initial reference on the scheduler, and returns a pointer to it.  
  
```  
static Scheduler * __cdecl Create(  
   const SchedulerPolicy&                 _Policy  
);  
```  
  
### Parameters  
 `_Policy`  
 The scheduler policy that describes behavior of the newly created scheduler.  
  
### Return Value  
 A pointer to a newly created scheduler. This                         `Scheduler` object has an initial reference count placed on it.  
  
### Remarks  
 After a scheduler is created with the                         `Create` method, you must call the                         `Release` method at some point in the future in order to remove the initial reference count and allow the scheduler to shut down.  
  
 A scheduler created with this method is not attached to the calling context. It can be attached to a context using the                         [Attach](#scheduler__attach_method) method.  
  
 This method can throw a variety of exceptions, including                         [scheduler_resource_allocation_error](../vs140/scheduler_resource_allocation_error-Class.md) and                         [invalid_scheduler_policy_value](../vs140/invalid_scheduler_policy_value-Class.md).  
  
##  <a name="scheduler__createschedulegroup_method"></a>  Scheduler::CreateScheduleGroup Method  
 Creates a new schedule group within the scheduler. The version that takes the parameter                 `_Placement` causes tasks within the newly created schedule group to be biased towards executing at the location specified by that parameter.  
  
```  
virtual ScheduleGroup * CreateScheduleGroup() =0;  
  
virtual ScheduleGroup * CreateScheduleGroup(  
   location&                 _Placement  
) =0;  
```  
  
### Parameters  
 `_Placement`  
 A reference to a location where the tasks within the schedule group will biased towards executing at.  
  
### Return Value  
 A pointer to the newly created schedule group. This                         `ScheduleGroup` object has an initial reference count placed on it.  
  
### Remarks  
 You must invoke the                         [Release](../vs140/ScheduleGroup-Class.md#schedulegroup__release_method) method on a schedule group when you are done scheduling work to it. The scheduler will destroy the schedule group when all work queued to it has completed.  
  
 Note that if you explicitly created this scheduler, you must release all references to schedule groups within it, before you release your references on the scheduler.  
  
##  <a name="scheduler__getnumberofvirtualprocessors_method"></a>  Scheduler::GetNumberOfVirtualProcessors Method  
 Returns the current number of virtual processors for the scheduler.  
  
```  
virtual unsigned int GetNumberOfVirtualProcessors() const =0;  
```  
  
### Return Value  
 The current number of virtual processors for the scheduler.  
  
##  <a name="scheduler__getpolicy_method"></a>  Scheduler::GetPolicy Method  
 Returns a copy of the policy that the scheduler was created with.  
  
```  
virtual SchedulerPolicy GetPolicy() const =0;  
```  
  
### Return Value  
 A copy of the policy that the scheduler was created with.  
  
##  <a name="scheduler__id_method"></a>  Scheduler::Id Method  
 Returns a unique identifier for the scheduler.  
  
```  
virtual unsigned int Id() const =0;  
```  
  
### Return Value  
 A unique identifier for the scheduler.  
  
##  <a name="scheduler__isavailablelocation_method"></a>  Scheduler::IsAvailableLocation Method  
 Determines whether a given location is available on the scheduler.  
  
```  
virtual bool IsAvailableLocation(  
   const location&                 _Placement  
) const =0;  
```  
  
### Parameters  
 `_Placement`  
 A reference to the location to query the scheduler about.  
  
### Return Value  
 An indication of whether or not the location specified by the                         `_Placement` argument is available on the scheduler.  
  
### Remarks  
 Note that the return value is an instantaneous sampling of whether the given location is available. In the presence of multiple schedulers, dynamic resource management can add or take away resources from schedulers at any point. Should this happen, the given location can change availability.  
  
##  <a name="scheduler__reference_method"></a>  Scheduler::Reference Method  
 Increments the scheduler reference count.  
  
```  
virtual unsigned int Reference() =0 ;  
```  
  
### Return Value  
 The newly incremented reference count.  
  
### Remarks  
 This is typically used to manage the lifetime of the scheduler for composition. When the reference count of a scheduler falls to zero, the scheduler will shut down and destruct itself after all work on the scheduler has completed.  
  
 The method will throw an                         [improper_scheduler_reference](../vs140/improper_scheduler_reference-Class.md) exception if the reference count prior to calling the                         `Reference` method was zero and the call is made from a context that is not owned by the scheduler.  
  
##  <a name="scheduler__registershutdownevent_method"></a>  Scheduler::RegisterShutdownEvent Method  
 Causes the Windows event handle passed in the                 `_Event` parameter to be signaled when the scheduler shuts down and destroys itself. At the time the event is signaled, all work that had been scheduled to the scheduler is complete. Multiple shutdown events can be registered through this method.  
  
```  
virtual void RegisterShutdownEvent(  
   HANDLE                 _Event  
) =0;  
```  
  
### Parameters  
 `_Event`  
 A handle to a Windows event object which will be signaled by the runtime when the scheduler shuts down and destroys itself.  
  
##  <a name="scheduler__release_method"></a>  Scheduler::Release Method  
 Decrements the scheduler reference count.  
  
```  
virtual unsigned int Release() =0;  
```  
  
### Return Value  
 The newly decremented reference count.  
  
### Remarks  
 This is typically used to manage the lifetime of the scheduler for composition. When the reference count of a scheduler falls to zero, the scheduler will shut down and destruct itself after all work on the scheduler has completed.  
  
##  <a name="scheduler__resetdefaultschedulerpolicy_method"></a>  Scheduler::ResetDefaultSchedulerPolicy Method  
 Resets the default scheduler policy to the runtime default. The next time a default scheduler is created, it will use the runtime default policy settings.  
  
```  
static void __cdecl ResetDefaultSchedulerPolicy();  
```  
  
### Remarks  
 This method can be called while a default scheduler exists within the process. It will not affect the policy of the existing default scheduler. However, if the default scheduler were to shutdown, and a new default were to be created at a later point, the new scheduler would use the runtime default policy settings.  
  
##  <a name="scheduler__scheduler_constructor"></a>  Scheduler::Scheduler Constructor  
 An object of the                 `Scheduler` class can only created using factory methods, or implicitly.  
  
```  
Scheduler();  
```  
  
### Remarks  
 The process' default scheduler is created implicitly when you utilize many of the runtime functions which require a scheduler to be attached to the calling context. Methods within the                         `CurrentScheduler` class and features of the PPL and agents layers typically perform implicit attachment.  
  
 You can also create a scheduler explicitly through either the                         `CurrentScheduler::Create` method or the                         `Scheduler::Create` method.  
  
##  <a name="scheduler___dtorscheduler_destructor"></a>  Scheduler::~Scheduler Destructor  
 An object of the                 `Scheduler` class is implicitly destroyed when all external references to it cease to exist.  
  
```  
virtual ~Scheduler();  
```  
  
##  <a name="scheduler__scheduletask_method"></a>  Scheduler::ScheduleTask Method  
 Schedules a light-weight task within the scheduler. The light-weight task will be placed in a schedule group determined by the runtime. The version that takes the parameter                 `_Placement` causes the task to be biased towards executing at the specified location.  
  
```  
virtual void ScheduleTask(  
   TaskProc                 _Proc,  
   _Inout_opt_ void *                 _Data  
) =0;  
  
virtual void ScheduleTask(  
   TaskProc                 _Proc,  
   _Inout_opt_ void *                 _Data,  
   location&                 _Placement  
) =0;  
```  
  
### Parameters  
 `_Proc`  
 A pointer to the function to execute to perform the body of the light-weight task.  
  
 `_Data`  
 A void pointer to the data that will be passed as a parameter to the body of the task.  
  
 `_Placement`  
 A reference to a location where the light-weight task will be biased towards executing at.  
  
##  <a name="scheduler__setdefaultschedulerpolicy_method"></a>  Scheduler::SetDefaultSchedulerPolicy Method  
 Allows a user defined policy to be used to create the default scheduler. This method can be called only when no default scheduler exists within the process. After a default policy has been set, it remains in effect until the next valid call to either the                 `SetDefaultSchedulerPolicy` or the                 [ResetDefaultSchedulerPolicy](#scheduler__resetdefaultschedulerpolicy_method) method.  
  
```  
static void __cdecl SetDefaultSchedulerPolicy(  
   const SchedulerPolicy&                 _Policy  
);  
```  
  
### Parameters  
 `_Policy`  
 The policy to be set as the default scheduler policy.  
  
### Remarks  
 If the                         `SetDefaultSchedulerPolicy` method is called when a default scheduler already exists within the process, the runtime will throw a                         [default_scheduler_exists](../vs140/default_scheduler_exists-Class.md) exception.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [PolicyElementKey Enumeration](concurrency_namespace_Enumerations)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)