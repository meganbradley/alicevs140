---
title: "accelerator Class"
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
ms.assetid: 37eed593-cf87-4611-9cdc-e98df6c2377a
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# accelerator Class
An accelerator is a hardware capability that is optimized for data-parallel computing. An accelerator may be a device attached to a PCIe bus (such as a GPU), or it might be an extended instruction set on the main CPU.  
  
## Syntax  
  
```  
class accelerator;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[accelerator::accelerator Constructor](#accelerator__accelerator_constructor)|Initializes a new instance of the                                         `accelerator` class.|  
|[accelerator::~accelerator Destructor](#accelerator___dtoraccelerator_destructor)|Destroys the                                         `accelerator` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[accelerator::create_view Method](#accelerator__create_view_method)|Creates and returns an                                         `accelerator_view` object on this accelerator.|  
|[accelerator::get_all Method](#accelerator__get_all_method)|Returns a vector of                                         `accelerator` objects that represent all the available accelerators.|  
|[accelerator::get_auto_selection_view Method](#accelerator__get_auto_selection_view_method)|Returns the auto-selection                                         `accelerator_view`.|  
|[accelerator::get_dedicated_memory Method](#accelerator__get_dedicated_memory_method)|Returns the dedicated memory for the                                         `accelerator`, in kilobytes.|  
|[accelerator::get_default_cpu_access_type Method](#accelerator__get_default_cpu_access_type_method)|Returns the default                                         [access_type](concurrency_namespace__c++_amp__Enumerations) for buffers created on this accelerator.|  
|[accelerator::get_default_view Method](#accelerator__get_default_view_method)|Returns the default                                         `accelerator_view` object that is associated with the                                         `accelerator`.|  
|[accelerator::get_description Method](#accelerator__get_description_method)|Returns a short description of the                                         `accelerator` device.|  
|[accelerator::get_device_path Method](#accelerator__get_device_path_method)|Returns the path of the device.|  
|[accelerator::get_has_display Method](#accelerator__get_has_display_method)|Determines whether the                                         `accelerator` is attached to a display.|  
|[accelerator::get_is_debug Method](#accelerator__get_is_debug_method)|Determines whether the                                         `accelerator` has the DEBUG layer enabled for extensive error reporting.|  
|[accelerator::get_is_emulated Method](#accelerator__get_is_emulated_method)|Determines whether the                                         `accelerator` is emulated.|  
|[accelerator::get_supports_cpu_shared_memory Method](#accelerator__get_supports_cpu_shared_memory_method)|Determines whether the                                         `accelerator` supports shared memory|  
|[accelerator::get_supports_double_precision Method](#accelerator__get_supports_double_precision_method)|Determines whether the                                         `accelerator` is attached to a display.|  
|[accelerator::get_supports_limited_double_precision Method](#accelerator__get_supports_limited_double_precision_method)|Determines whether the                                         `accelerator` has limited support for double-precision math.|  
|[accelerator::get_version Method](#accelerator__get_version_method)|Returns the version of the                                         `accelerator`.|  
|[accelerator::set_default Method](#accelerator__set_default_method)|Returns the path of the default accelerator.|  
|[Accelerator::set_default_cpu_access_type Method](#accelerator__set_default_cpu_access_type_method)|Sets the default CPU                                         [access_type](concurrency_namespace__c++_amp__Enumerations) for arrays and implicit memory allocations made on this                                         `accelerator`.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[accelerator::operator!= Operator](#accelerator__operator_neq_operator)|Compares this                                         `accelerator` object with another and returns                                         `false` if they are the same; otherwise, returns                                         `true`.|  
|[accelerator::operator= Operator](#accelerator__operator_eq_operator)|Copies the contents of the specified                                         `accelerator` object to this one.|  
|[accelerator::operator== Operator](#accelerator__operator_eq_eq_operator)|Compares this                                         `accelerator` object with another and returns                                         `true` if they are the same; otherwise, returns                                         `false`.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[accelerator::cpu_accelerator Data Member](#accelerator__cpu_accelerator_data_member)|Gets a string constant for the CPU                                         `accelerator`.|  
|[accelerator::dedicated_memory Data Member](#accelerator__dedicated_memory_data_member)|Gets the dedicated memory for the                                         `accelerator`, in kilobytes.|  
|[accelerator::default_accelerator Data Member](#accelerator__default_accelerator_data_member)|Gets a string constant for the default                                         `accelerator`.|  
|[accelerator::default_cpu_access_type Data Member](#accelerator__default_cpu_access_type_data_member)|Gets or sets the default CPU                                         [access_type](concurrency_namespace__c++_amp__Enumerations) for arrays and implicit memory allocations made on this                                         `accelerator`.|  
|[accelerator::default_view Data Member](#accelerator__default_view_data_member)|Gets the default                                         `accelerator_view` object that is associated with the                                         `accelerator`.|  
|[accelerator::description Data Member](#accelerator__description_data_member)|Gets a short description of the                                         `accelerator` device.|  
|[accelerator::device_path Data Member](#accelerator__device_path_data_member)|Gets the path of the device.|  
|[accelerator::direct3d_ref Data Member](#accelerator__direct3d_ref_data_member)|Gets a string constant for a Direct3D reference                                         `accelerator`.|  
|[accelerator::direct3d_warp Data Member](#accelerator__direct3d_warp_data_member)|Gets the string constant for an                                         [accelerator](../vs140/accelerator-Class.md) object that you can use for executing C++ AMP code on multi-core CPUs that use Streaming SIMD Extensions (SSE).|  
|[accelerator::has_display Data Member](#accelerator__has_display_data_member)|Gets a Boolean value that indicates whether the                                         `accelerator` is attached to a display.|  
|[accelerator::is_debug Data Member](#accelerator__is_debug_data_member)|Indicates whether the                                         `accelerator` has the DEBUG layer enabled for extensive error reporting.|  
|[accelerator::is_emulated Data Member](#accelerator__is_emulated_data_member)|Indicates whether the                                         `accelerator` is emulated.|  
|[Accelerator::supports_cpu_shared_memory Data Member](#accelerator__supports_cpu_shared_memory_data_member)|Indicates whether the                                         `accelerator` supports shared memory.|  
|[accelerator::supports_double_precision Data Member](#accelerator__supports_double_precision_data_member)|Indicates whether the accelerator supports double-precision math.|  
|[accelerator::supports_limited_double_precision Data Member](#accelerator__supports_limited_double_precision_data_member)|Indicates whether the accelerator has limited support for double-precision math.|  
|[accelerator::version Data Member](#accelerator__version_data_member)|Gets the version of the                                         `accelerator`.|  
  
## Inheritance Hierarchy  
 `accelerator`  
  
## Remarks  
 An accelerator is a hardware capability that is optimized for data-parallel computing. An accelerator is often a discrete GPU, but it can also be a virtual host-side entity such as a DirectX REF device, a WARP (a CPU-side device that is accelerated by means of SSE instructions), or the CPU itself.  
  
 You can construct an                 `accelerator` object by enumerating the available devices, or by getting the default device, the reference device, or the WARP device.  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
##  <a name="accelerator___dtoraccelerator_destructor"></a>  accelerator::~accelerator Destructor  
 Destroys the                 [accelerator](../vs140/accelerator-Class.md) object.  
  
```  
~accelerator();  
```  
  
### Return Value  
  
##  <a name="accelerator__accelerator_constructor"></a>  accelerator::accelerator Constructor  
 Initializes a new instance of the                 [accelerator class](../vs140/accelerator-Class.md).  
  
```  
accelerator();  
  
explicit accelerator(  
   const std::wstring &                _Device_path  
);  
  
accelerator(  
   const accelerator &                _Other  
);  
```  
  
### Parameters  
 `_Device_path`  
 The path of the physical device.  
  
 `_Other`  
 The accelerator to copy.  
  
##  <a name="accelerator__cpu_accelerator_data_member"></a>  accelerator::cpu_accelerator Data Member  
 Gets a string constant for the CPU accelerator.  
  
```  
static const wchar_t cpu_accelerator[];  
```  
  
##  <a name="accelerator__create_view_method"></a>  accelerator::create_view Method  
 Creates and returns an                 `accelerator_view` object on this accelerator, using the specified queuing mode. When the queuing mode is not specified, the new                 `accelerator_view` uses the                 [queuing_mode::immediate](concurrency_namespace__c++_amp__Enumerations) queuing mode.  
  
```  
accelerator_view create_view(  
   queuing_mode                 qmode = queuing_mode_automatic  
);  
```  
  
### Parameters  
 `qmode`  
 The queuing mode.  
  
### Return Value  
 A new                         `accelerator_view` object on this accelerator, using the specified queuing mode.  
  
##  <a name="accelerator__dedicated_memory_data_member"></a>  accelerator::dedicated_memory Data Member  
 Gets the dedicated memory for the                 [accelerator](../vs140/accelerator-Class.md), in kilobytes.  
  
```  
__declspec(property(get=get_dedicated_memory)) size_t dedicated_memory;  
```  
  
##  <a name="accelerator__default_accelerator_data_member"></a>  accelerator::default_accelerator Data Member  
 Gets a string constant for the default                 [accelerator](../vs140/accelerator-Class.md).  
  
```  
static const wchar_t default_accelerator[];  
```  
  
##  <a name="accelerator__default_cpu_access_type_data_member"></a>  accelerator::default_cpu_access_type Data Member  
 The default cpu                 [access_type](concurrency_namespace__c++_amp__Enumerations) for arrays and implicit memory allocations made on this this                 `accelerator`.  
  
```  
__declspec(property(get=get_default_cpu_access_type)) access_type default_cpu_access_type;  
```  
  
##  <a name="accelerator__default_view_data_member"></a>  accelerator::default_view Data Member  
 Gets the default accelerator view that is associated with the                 [accelerator](../vs140/accelerator-Class.md).  
  
```  
__declspec(property(get=get_default_view)) accelerator_view default_view;  
```  
  
##  <a name="accelerator__description_data_member"></a>  accelerator::description Data Member  
 Gets a short description of the                 [accelerator](../vs140/accelerator-Class.md) device.  
  
```  
__declspec(property(get=get_description)) std::wstring description;  
```  
  
##  <a name="accelerator__device_path_data_member"></a>  accelerator::device_path Data Member  
 Gets the path of the accelerator. The path is unique on the system.  
  
```  
__declspec(property(get=get_device_path)) std::wstring device_path;  
```  
  
##  <a name="accelerator__direct3d_ref_data_member"></a>  accelerator::direct3d_ref Data Member  
 Gets a string constant for a Direct3D reference accelerator.  
  
```  
static const wchar_t direct3d_ref[];  
```  
  
##  <a name="accelerator__direct3d_warp_data_member"></a>  accelerator::direct3d_warp Data Member  
 Gets the string constant for an                 [accelerator](../vs140/accelerator-Class.md) object that you can use for executing your C++ AMP code on multi-core CPUs using Streaming SIMD Extensions (SSE).  
  
```  
static const wchar_t direct3d_warp[];  
```  
  
##  <a name="accelerator__get_all_method"></a>  accelerator::get_all Method  
 Returns a vector of                 `accelerator` objects that represent all the available accelerators.  
  
```  
static inline std::vector<accelerator> get_all();  
```  
  
### Return Value  
 The vector of available accelerators  
  
##  <a name="accelerator__get_auto_selection_view_method"></a>  accelerator::get_auto_selection_view Method  
 Returns the auto selection accelerator_view, which when specified as the parallel_for_each target results in the target accelerator_view for executing the parallel_for_each kernel to be automatically selected by the runtime. For all other purposes, the accelerator_view returned by this method is the same as the default accelerator_view of the default accelerator  
  
```  
static accelerator_view __cdecl get_auto_selection_view();  
```  
  
### Return Value  
 The auto selection accelerator_view.  
  
##  <a name="accelerator__get_dedicated_memory_method"></a>  accelerator::get_dedicated_memory Method  
 Returns the dedicated memory for the                 [accelerator](../vs140/accelerator-Class.md), in kilobytes.  
  
```  
size_t get_dedicated_memory() const;  
```  
  
### Return Value  
 The dedicated memory for the                         `accelerator`, in kilobytes.  
  
##  <a name="accelerator__get_default_cpu_access_type_method"></a>  accelerator::get_default_cpu_access_type Method  
 Gets the default cpu access_type for buffers created on this accelerator  
  
```  
access_type get_default_cpu_access_type() const;  
```  
  
### Return Value  
 The default cpu access_type for buffers created on this accelerator.  
  
##  <a name="accelerator__get_default_view_method"></a>  accelerator::get_default_view Method  
 Returns the default                 `accelerator_view` object that is associated with the                 [accelerator](../vs140/accelerator-Class.md).  
  
```  
accelerator_view get_default_view() const;  
```  
  
### Return Value  
 The default                         `accelerator_view` object that is associated with the                         `accelerator`.  
  
##  <a name="accelerator__get_description_method"></a>  accelerator::get_description Method  
 Returns a short description of the                 [accelerator](../vs140/accelerator-Class.md) device.  
  
```  
std::wstring get_description() const;  
```  
  
### Return Value  
 A short description of the                         `accelerator` device.  
  
##  <a name="accelerator__get_device_path_method"></a>  accelerator::get_device_path Method  
 Returns the path of the accelerator. The path is unique on the system.  
  
```  
std::wstring get_device_path() const;  
```  
  
### Return Value  
 The system-wide unique device instance path.  
  
##  <a name="accelerator__get_has_display_method"></a>  accelerator::get_has_display Method  
 Returns a Boolean value that indicates whether the                 [accelerator](../vs140/accelerator-Class.md) can output to a display.  
  
```  
bool get_has_display() const;  
```  
  
### Return Value  
 `true` if the                         `accelerator` can output to a display; otherwise,                         `false`.  
  
##  <a name="accelerator__get_is_debug_method"></a>  accelerator::get_is_debug Method  
 Determines whether the                 [accelerator](../vs140/accelerator-Class.md) has the DEBUG layer enabled for extensive error reporting.  
  
```  
bool get_is_debug() const;  
```  
  
### Return Value  
 `true` if the                         `accelerator` has the DEBUG layer enabled for extensive error reporting. Otherwise,                         `false`.  
  
##  <a name="accelerator__get_is_emulated_method"></a>  accelerator::get_is_emulated Method  
 Determines whether the                 [accelerator](../vs140/accelerator-Class.md) is emulated.  
  
```  
bool get_is_emulated() const;  
```  
  
### Return Value  
 `true` if the                         `accelerator` is emulated. Otherwise,                         `false`.  
  
##  <a name="accelerator__get_supports_cpu_shared_memory_method"></a>  accelerator::get_supports_cpu_shared_memory Method  
 Returns a boolean value indicating whether the accelerator supports memory accessible both by the accelerator and the CPU.  
  
```  
bool get_supports_cpu_shared_memory() const;  
```  
  
### Return Value  
 `true` if the accelerator supports CPU shared memory; otherwise,                         `false`.  
  
##  <a name="accelerator__get_supports_double_precision_method"></a>  accelerator::get_supports_double_precision Method  
 Returns a Boolean value that indicates whether the accelerator supports double precision math, including fused multiply add (FMA), division, reciprocal, and casting between                 `int` and                 `double`.  
  
```  
bool get_supports_double_precision() const;  
```  
  
### Return Value  
 `true` if the accelerator supports double precision math; otherwise,                         `false`.  
  
##  <a name="accelerator__get_supports_limited_double_precision_method"></a>  accelerator::get_supports_limited_double_precision Method  
 Returns a Boolean value that indicates whether the accelerator has limited support for double precision math. If the accelerator has only limited support, then fused multiply add (FMA), division, reciprocal, and casting between                 `int` and                 `double` are not supported.  
  
```  
bool get_supports_limited_double_precision() const;  
```  
  
### Return Value  
 `true` if the accelerator has limited support for double precision math; otherwise,                         `false`.  
  
##  <a name="accelerator__get_version_method"></a>  accelerator::get_version Method  
 Returns the version of the                 [accelerator](../vs140/accelerator-Class.md).  
  
```  
unsigned int get_version() const;  
```  
  
### Return Value  
 The version of the                         `accelerator`.  
  
##  <a name="accelerator__has_display_data_member"></a>  accelerator::has_display Data Member  
 Gets a Boolean value that indicates whether the                 [accelerator](../vs140/accelerator-Class.md) can output to a display.  
  
```  
__declspec(property(get=get_has_display)) bool has_display;  
```  
  
##  <a name="accelerator__is_debug_data_member"></a>  accelerator::is_debug Data Member  
 Gets a Boolean value that indicates whether the                 [accelerator](../vs140/accelerator-Class.md) has the DEBUG layer enabled for extensive error reporting.  
  
```  
__declspec(property(get=get_is_debug)) bool is_debug;  
```  
  
##  <a name="accelerator__is_emulated_data_member"></a>  accelerator::is_emulated Data Member  
 Gets a Boolean value that indicates whether the                 [accelerator](../vs140/accelerator-Class.md) is emulated.  
  
```  
__declspec(property(get=get_is_emulated)) bool is_emulated;  
```  
  
##  <a name="accelerator__operator_neq_operator"></a>  accelerator::operator!= Operator  
 Compares this                 `accelerator` object with another and returns                 `false` if they are the same; otherwise, returns                 `true`.  
  
```  
bool operator!=(  
   const accelerator &                _Other                       
) const;  
```  
  
### Parameters  
 `_Other`  
 The                                 `accelerator` object to compare with this one.  
  
### Return Value  
 `false` if the two                         `accelerator` objects are the same; otherwise,                         `true`.  
  
##  <a name="accelerator__operator_eq_operator"></a>  accelerator::operator= Operator  
 Copies the contents of the specified                 [accelerator](../vs140/accelerator-Class.md) object to this one.  
  
```  
accelerator &operator=(  
   const accelerator &                _Other                       
);  
```  
  
### Parameters  
 `_Other`  
 The                                 `accelerator` object to copy from.  
  
### Return Value  
 A reference to this                         `accelerator` object.  
  
##  <a name="accelerator__operator_eq_eq_operator"></a>  accelerator::operator== Operator  
 Compares this                 [accelerator](../vs140/accelerator-Class.md) object with another and returns                 `true` if they are the same; otherwise, returns                 `false`.  
  
```  
bool operator==(  
   const accelerator &                _Other                       
) const;  
```  
  
### Parameters  
 `_Other`  
 The                                 `accelerator` object to compare with this one.  
  
### Return Value  
 `true` if the other                         `accelerator` object is same as this                         `accelerator` object; otherwise,                         `false`.  
  
##  <a name="accelerator__set_default_method"></a>  accelerator::set_default Method  
 Sets the default accelerator to be used for any operation that implicitly uses the default accelerator. This method only succeeds if the runtime selected default accelerator has not already been used in an operation that implicitly uses the default accelerator  
  
```  
static inline bool set_default(  
   std::wstring                 _Path  
);  
```  
  
### Parameters  
 `_Path`  
 The path to the accelerator.  
  
### Return Value  
 `true` if the call succeeds at setting the default accelerator. Otherwise,                         `false`.  
  
##  <a name="accelerator__set_default_cpu_access_type_method"></a>  accelerator::set_default_cpu_access_type Method  
 Set the default cpu access_type for arrays created on this accelerator or for implicit memory allocations as part of array_views accessed on this this accelerator. This method only succeeds if the default_cpu_access_type for the accelerator has not already been overriden by a previous call to this method and the runtime selected default_cpu_access_type for this accelerator has not yet been used for allocating an array or for an implicit memory allocation backing an array_view accessed on this accelerator.  
  
```  
bool set_default_cpu_access_type(  
   access_type                 _Default_cpu_access_type  
);  
```  
  
### Parameters  
 `_Default_cpu_access_type`  
 The default cpu access_type to be used for array/array_view memory allocations on this accelerator.  
  
### Return Value  
 A boolean value indicating if the default cpu access_type for the accelerator was successfully set.  
  
##  <a name="accelerator__supports_cpu_shared_memory_data_member"></a>  accelerator::supports_cpu_shared_memory Data Member  
 Gets a Boolean value indicating whether the                 `accelerator` supports shared memory.  
  
```  
__declspec(property(get=get_supports_cpu_shared_memory)) bool supports_cpu_shared_memory;  
```  
  
##  <a name="accelerator__supports_double_precision_data_member"></a>  accelerator::supports_double_precision Data Member  
 Gets a Boolean value that indicates whether the accelerator supports double precision math.  
  
```  
__declspec(property(get=get_supports_double_precision)) bool supports_double_precision;  
```  
  
##  <a name="accelerator__supports_limited_double_precision_data_member"></a>  accelerator::supports_limited_double_precision Data Member  
 Gets a Boolean value that indicates whether the accelerator has limited support for double precision math. If the accelerator has only limited support, then fused multiply add (FMA), division, reciprocal, and casting between                 `int` and                 `double` are not supported.  
  
```  
__declspec(property(get=get_supports_limited_double_precision)) bool supports_limited_double_precision;  
```  
  
##  <a name="accelerator__version_data_member"></a>  accelerator::version Data Member  
 Gets the version of the                 [accelerator](../vs140/accelerator-Class.md).  
  
```  
__declspec(property(get=get_version)) unsigned int version;  
```  
  
##  <a name="accelerator_view___dtoraccelerator_view_destructor"></a>  accelerator_view::~accelerator_view Destructor  
 Destroys the                  [accelerator_view](../vs140/accelerator_view-Class.md) object.  
  
```  
~accelerator_view();  
```  
  
### Return Value  
  
##  <a name="accelerator_view__accelerator_data_member"></a>  accelerator_view::accelerator Data Member  
 Gets the                  [accelerator](../vs140/accelerator-Class.md) object for the                  [accelerator_view](../vs140/accelerator_view-Class.md) object.  
  
```  
__declspec(property(get=get_accelerator)) Concurrency::accelerator accelerator;  
```  
  
##  <a name="accelerator_view__accelerator_view_constructor"></a>  accelerator_view::accelerator_view Constructor  
 Initializes a new instance of the                 [accelerator_view](../vs140/accelerator_view-Class.md) class by copying an existing                 `accelerator_view` object.  
  
```  
accelerator_view(  
   const accelerator_view &                _Other  
  
);  
```  
  
### Parameters  
 `_Other`  
 The                                 `accelerator_view` object to copy.  
  
##  <a name="accelerator_view__create_marker_method"></a>  accelerator_view::create_marker Method  
 Returns a future to track the completion of all commands submitted so far to this                 `accelerator_view` object.  
  
```  
concurrency::completion_future create_marker();  
```  
  
### Return Value  
 A future to track the completion of all commands submitted so far to this                         `accelerator_view` object.  
  
##  <a name="accelerator_view__flush_method"></a>  accelerator_view::flush Method  
 Submits all pending commands queued to the                 [accelerator_view](../vs140/accelerator_view-Class.md) object to the accelerator for execution.  
  
```  
void flush();  
```  
  
### Return Value  
 Returns                         `void`.  
  
##  <a name="accelerator_view__get_accelerator_method"></a>  accelerator_view::get_accelerator Method  
 Returns the                 [accelerator](../vs140/accelerator-Class.md) object for the                  [accelerator_view](../vs140/accelerator_view-Class.md) object.  
  
```  
accelerator get_accelerator() const;  
```  
  
### Return Value  
 The                         `accelerator` object for the                         `accelerator_view` object.  
  
##  <a name="accelerator_view__get_is_auto_selection_method"></a>  accelerator_view::get_is_auto_selection Method  
 Returns a Boolean value that indicates whether the runtime will automatically select an appropriate accelerator when the accelerator_view is passed to a                 [parallel_for_each](concurrency_namespace__c++_amp__Functions).  
  
```  
bool get_is_auto_selection() const;  
```  
  
### Return Value  
 `true` if the runtime will automatically select an appropriate accelerator; otherwise,                         `false`.  
  
##  <a name="accelerator_view__get_is_debug_method"></a>  accelerator_view::get_is_debug Method  
 Returns a Boolean value that indicates whether the                 [accelerator_view](../vs140/accelerator_view-Class.md) object has the DEBUG layer enabled for extensive error reporting.  
  
```  
bool get_is_debug() const;  
```  
  
### Return Value  
 A Boolean value that indicates whether the                         `accelerator_view` object has the DEBUG layer enabled for extensive error reporting.  
  
##  <a name="accelerator_view__get_queuing_mode_method"></a>  accelerator_view::get_queuing_mode Method  
 Returns the queuing mode for the                 [accelerator_view](../vs140/accelerator_view-Class.md) object.  
  
```  
queuing_mode get_queuing_mode() const;  
```  
  
### Return Value  
 The queuing mode for the                         `accelerator_view` object.  
  
##  <a name="accelerator_view__get_version_method"></a>  accelerator_view::get_version Method  
 Returns the version of the                 [accelerator_view](../vs140/accelerator_view-Class.md).  
  
```  
unsigned int get_version() const;  
```  
  
### Return Value  
 The version of the                         `accelerator_view`.  
  
##  <a name="accelerator_view__is_auto_selection_data_member"></a>  accelerator_view::is_auto_selection Data Member  
 Gets a Boolean value that indicates whether the runtime will automatically select an appropriate accelerator when the accelerator_view is passed to a                 [parallel_for_each](concurrency_namespace__c++_amp__Functions).  
  
```  
__declspec(property(get=get_is_auto_selection)) bool is_auto_selection;  
```  
  
##  <a name="accelerator_view__is_debug_data_member"></a>  accelerator_view::is_debug Data Member  
 Gets a Boolean value that indicates whether the                 [accelerator_view](../vs140/accelerator_view-Class.md) object has the  DEBUG layer enabled for extensive error reporting.  
  
```  
__declspec(property(get=get_is_debug)) bool is_debug;  
```  
  
##  <a name="accelerator_view__operator_neq_operator"></a>  accelerator_view::operator!= Operator  
 Compares this                 [accelerator_view](../vs140/accelerator_view-Class.md) object with another and returns                 `false` if they are the same; otherwise, returns                 `true`.  
  
```  
bool operator!=(  
   const accelerator_view &                _Other  
  
) const;  
```  
  
### Parameters  
 `_Other`  
 The                                 `accelerator_view` object to compare with this one.  
  
### Return Value  
 `false` if the two objects are the same; otherwise,                         `true`.  
  
##  <a name="accelerator_view__operator_eq_operator"></a>  accelerator_view::operator= Operator  
 Copies the contents of the specified                  [accelerator_view](../vs140/accelerator_view-Class.md) object into this one.  
  
```  
accelerator_view &operator=(  
   const accelerator_view &                _Other                       
);  
```  
  
### Parameters  
 `_Other`  
 The                                 `accelerator_view` object to copy from.  
  
### Return Value  
 A reference to the modified                         `accelerator_view` object.  
  
##  <a name="accelerator_view__operator_eq_eq_operator"></a>  accelerator_view::operator== Operator  
 Compares this                 [accelerator_view](../vs140/accelerator_view-Class.md) object with another and returns                 `true` if they are the same; otherwise, returns                 `false`.  
  
```  
bool operator==(  
   const accelerator_view &                _Other                       
) const;  
```  
  
### Parameters  
 `_Other`  
 The                                 `accelerator_view` object to compare with this one.  
  
### Return Value  
 `true` if the two objects are the same; otherwise,                         `false`.  
  
##  <a name="accelerator_view__queuing_mode_data_member"></a>  accelerator_view::queuing_mode Data Member  
 Gets the queuing mode for the                  [accelerator_view](../vs140/accelerator_view-Class.md) object.  
  
```  
__declspec(property(get=get_queuing_mode)) Concurrency::queuing_mode queuing_mode;  
```  
  
##  <a name="accelerator_view__version_data_member"></a>  accelerator_view::version Data Member  
 Gets the version of the                 [accelerator_view](../vs140/accelerator_view-Class.md).  
  
```  
__declspec(property(get=get_version)) unsigned int version;  
```  
  
##  <a name="accelerator_view__wait_method"></a>  accelerator_view::wait Method  
 Waits for all commands submitted to the                  [accelerator_view](../vs140/accelerator_view-Class.md) object to finish.  
  
```  
void wait();  
```  
  
### Return Value  
 Returns                         `void`.  
  
## See Also  
 [Concurrency Namespace (C++ Accelerated Massive Parallelism)](../vs140/Concurrency-Namespace--C---AMP-.md)