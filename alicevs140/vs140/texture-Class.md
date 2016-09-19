---
title: "texture Class"
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
ms.assetid: 16e85d4d-e80a-474a-995d-8bf63fbdf34c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# texture Class
A texture is a data aggregate on an             `accelerator_view` in the extent domain. It is a collection of variables, one for each element in an extent domain. Each variable holds a value corresponding to C++ primitive type (            `unsigned int`,             `int`,             `float`,             `double`), a scalar type (            `norm`, or             `unorm`), or a short vector type.  
  
## Syntax  
  
```  
template <  
   typename             _Value_type,  
   int             _Rank  
>  
class texture;  
```  
  
#### Parameters  
 `_Value_type`  
 The type of the elements in the texture.  
  
 `_Rank`  
 The rank of the texture.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`scalar_type`|Scalar types.|  
|`value_type`|Value types.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[texture::texture Constructor](#texture__texture_constructor)|Initializes a new instance of the                                         [texture](../vs140/texture-Class.md) class.|  
|[texture::~texture Destructor](#texture___dtortexture_destructor)|Destroys the                                         [texture](../vs140/texture-Class.md) object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[texture::copy_to Method](#texture__copy_to_method)|Copies the                                         [texture](../vs140/texture-Class.md) object to the destination, by doing a deep copy.|  
|[texture::data Method](#texture__data_method)|Returns a CPU pointer to the raw data of this texture.|  
|[texture::get Method](#texture__get_method)|Returns the value of the element at the specified index.|  
|[Texture::get_associated_accelerator_view Data Member](#texture__get_associated_accelerator_view_method)|Returns the                                         [accelerator_view](../vs140/accelerator_view-Class.md) that is the preferred target for this texture to be copied to.|  
|[texture::get_depth_pitch Method](#texture__get_depth_pitch_method)|Returns the number of bytes between each depth slice in a 3D staging texture on the CPU.|  
|[texture::get_row_pitch Method](#texture__get_row_pitch_method)|Returns the number of bytes between each row in a 2D or 3D staging texture on the CPU.|  
|[texture::set Method](#texture__set_method)|Sets the value of the element at the specified index.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[texture::operator() Operator](#texture__operator___operator)|Returns the element value that is specified by the parameters.|  
|[texture::operator&#91;&#93; Operator](#texture__operator_at_operator)|Returns the element that is at the specified index.|  
|[texture::operator= Operator](#texture__operator_eq_operator)|Copies the specified                                         [texture](../vs140/texture-Class.md) object to this one.|  
  
### Public Constants  
  
|Name|Description|  
|----------|-----------------|  
|[texture::rank Constant](#texture__rank_constant)|Gets the rank of the                                         [texture](../vs140/texture-Class.md) object.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[Texture::associated_accelerator_view Data Member](#texture__associated_accelerator_view_data_member)|Gets the                                         [accelerator_view](../vs140/accelerator_view-Class.md) that is the preferred target for this texture to be copied to.|  
|[texture::depth_pitch Data Member](#texture__depth_pitch_data_member)|Gets the number of bytes between each depth slice in a 3D staging texture on the CPU.|  
|[texture::row_pitch Data Member](#texture__row_pitch_data_member)|Gets the number of bytes between each row in a 2D or 3D staging texture on the CPU.|  
  
## Inheritance Hierarchy  
 `_Texture_base`  
  
 `texture`  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** Concurrency::graphics  
  
##  <a name="texture___dtortexture_destructor"></a>  texture::~texture Destructor  
 Destroys the                 [texture](../vs140/texture-Class.md) object.  
  
```  
~texture() restrict(cpu);  
```  
  
##  <a name="texture__associated_accelerator_view_data_member"></a>  texture::associated_accelerator_view Data Member  
 Gets the                 [accelerator_view](../vs140/accelerator_view-Class.md) that is the preferred target for this texture to be copied to.  
  
```  
__declspec(property(get=get_associated_accelerator_view)) Concurrency::accelerator_view associated_accelerator_view;  
```  
  
##  <a name="texture__copy_to_method"></a>  texture::copy_to Method  
 Copies the                 [texture](../vs140/texture-Class.md) object to the destination, by doing a deep copy.  
  
```  
void copy_to(  
   texture &                 _Dest  
) const;  
  
void copy_to(  
   writeonly_texture_view<_Value_type, _Rank> &                 _Dest  
) const;  
```  
  
### Parameters  
 `_Dest`  
 The object to copy to.  
  
 `_Rank`  
 The rank of the texture.  
  
 `_Value_type`  
 The type of the elements in the texture.  
  
##  <a name="texture__data_method"></a>  texture::data Method  
 Returns a CPU pointer to the raw data of this texture.  
  
```  
void* data() restrict(cpu);  
  
const void* data() const restrict(cpu);  
```  
  
### Return Value  
 A pointer to the raw data of the texture.  
  
##  <a name="texture__depth_pitch_data_member"></a>  texture::depth_pitch Data Member  
 Gets the number of bytes between each depth slice in a 3D staging texture on the CPU.  
  
```  
__declspec(property(get=get_depth_pitch)) unsigned int depth_pitch;  
```  
  
##  <a name="texture__get_method"></a>  texture::get Method  
 Returns the value of the element at the specified index.  
  
```  
const value_type get(  
   const index<_Rank>&                 _Index  
) const restrict(amp);  
```  
  
### Parameters  
 `_Index`  
 The index of the element.  
  
### Return Value  
 The value of the element at the specified index.  
  
##  <a name="texture__get_associated_accelerator_view_method"></a>  texture::get_associated_accelerator_view Method  
 Returns the accelerator_view that is the preferred target for this texture to be copied to.  
  
```  
Concurrency::accelerator_view get_associated_accelerator_view() const restrict(cpu);  
```  
  
### Return Value  
 The                         [accelerator_view](../vs140/accelerator_view-Class.md) that is the preferred target for this texture to be copied to.  
  
##  <a name="texture__get_depth_pitch_method"></a>  texture::get_depth_pitch Method  
 Returns the number of bytes between each depth slice in a 3D staging texture on the CPU.  
  
```  
unsigned int get_depth_pitch() const restrict(cpu);  
```  
  
### Return Value  
 The number of bytes between each depth slice in a 3D staging texture on the CPU.  
  
##  <a name="texture__get_row_pitch_method"></a>  texture::get_row_pitch Method  
 Returns the number of bytes between each row in a 2-dimensional staging texture, or between each row of a depth slice in 3-dimensional staging texture.  
  
```  
unsigned int get_row_pitch() const restrict(cpu);  
```  
  
### Return Value  
 The number of bytes between each row in a 2-dimensional staging texture, or between each row of a depth slice in 3-dimensional staging texture.  
  
##  <a name="texture__operator___operator"></a>  texture::operator() Operator  
 Returns the element value that is specified by the parameters.  
  
```  
const value_type operator() (  
   const index<_Rank>&                 _Index  
) const restrict(amp);  
  
const value_type operator() (  
   int                 _I0  
) const restrict(amp);  
  
const value_type operator() (  
   int                 _I0,  
   int                 _I1  
) const restrict(amp);  
  
const value_type operator() (  
   int                 _I0,  
   int                 _I1,  
   int                 _I2  
) const restrict(amp);  
```  
  
### Parameters  
 `_Index`  
 The index.  
  
 `_I0`  
 The most-significant component of the index.  
  
 `_I1`  
 The next-to-most-significant component of the index.  
  
 `_I2`  
 The least-significant component of the index.  
  
 `_Rank`  
 The rank of the index.  
  
### Return Value  
 The element value that is specified by the parameters.  
  
##  <a name="texture__operator_at_operator"></a>  texture::operator[] Operator  
 Returns the element that is at the specified index.  
  
```  
const value_type operator[] (  
   const index<_Rank>&                 _Index  
) const restrict(amp);  
  
const value_type operator[] (  
   int                 _I0  
) const restrict(amp);  
```  
  
### Parameters  
 `_Index`  
 The index.  
  
 `_I0`  
 The index.  
  
### Return Value  
 The element that is at the specified index.  
  
##  <a name="texture__operator_eq_operator"></a>  texture::operator= Operator  
 Copies the specified                 [texture](../vs140/texture-Class.md) object to this one.  
  
```  
texture& operator=(  
   const texture &                 _Other  
);  
  
texture& operator=(  
   texture<_Value_type, _Rank> &&                 _Other  
);  
```  
  
### Parameters  
 `_Other`  
 The                                 [texture](../vs140/texture-Class.md) object to copy from.  
  
### Return Value  
 A reference to this                         [texture](../vs140/texture-Class.md) object.  
  
##  <a name="texture__rank_constant"></a>  texture::rank Constant  
 Gets the rank of the                 [texture](../vs140/texture-Class.md) object.  
  
```  
static const int rank = _Rank;  
```  
  
##  <a name="texture__row_pitch_data_member"></a>  texture::row_pitch Data Member  
 Gets the number of bytes between each row in a 2D or 3D staging texture on the CPU.  
  
```  
__declspec(property(get=get_row_pitch)) unsigned int row_pitch;  
```  
  
##  <a name="texture__set_method"></a>  texture::set Method  
 Sets the value of the element at the specified index.  
  
```  
void set(  
   const index<_Rank>&                 _Index,  
   const value_type&                 _Value  
) restrict(amp);  
```  
  
### Parameters  
 `_Index`  
 The index of the element.  
  
 `_Rank`  
 The rank of the index.  
  
 `_Value`  
 The new value of the element.  
  
##  <a name="texture__texture_constructor"></a>  texture::texture Constructor  
 Initializes a new instance of the                 [texture](../vs140/texture-Class.md) class.  
  
```  
texture(  
   const Concurrency::extent<_Rank>&                 _Ext  
) restrict(cpu);  
  
texture(  
   int                 _E0  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   int                 _E2  
) restrict(cpu);  
  
texture(  
   const Concurrency::extent<_Rank>&                 _Ext,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   int                 _E2,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
template<  
   typename                 _Input_iterator  
>  
texture(  
   const Concurrency::extent<_Rank>&                 _Ext,  
                   _Input_iterator  
                _Src_first,  
                   _Input_iterator  
                _Src_last  
) restrict(cpu);  
  
template<  
   typename                 _Input_iterator  
>  
texture(  
   int                 _E0,  
                   _Input_iterator  
                _Src_first,  
                   _Input_iterator  
                _Src_last  
) restrict(cpu);  
  
template<  
   typename                 _Input_iterator  
>  
texture(  
   int                 _E0,  
   int                 _E1,  
                   _Input_iterator  
                _Src_first,  
                   _Input_iterator  
                _Src_last  
) restrict(cpu);  
  
template<  
   typename                 _Input_iterator  
>  
texture(  
   int                 _E0,  
   int                 _E1,  
   int                 _E2,  
                   _Input_iterator  
                _Src_first,  
                   _Input_iterator  
                _Src_last  
) restrict(cpu);  
  
template<  
   typename                 _Input_iterator  
>  
texture(  
   const Concurrency::extent<_Rank>&                 _Ext,  
                   _Input_iterator  
                _Src_first,  
                   _Input_iterator  
                _Src_last,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
template<  
   typename                 _Input_iterator  
>  
texture(  
   int                 _E0,  
                   _Input_iterator  
                _Src_first,  
                   _Input_iterator  
                _Src_last,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
template<  
   typename                 _Input_iterator  
>  
texture(  
   int                 _E0,  
   int                 _E1,  
                   _Input_iterator  
                _Src_first,  
                   _Input_iterator  
                _Src_last,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
template<  
   typename                 _Input_iterator  
>  
texture(  
   int                 _E0,  
   int                 _E1,  
   int                 _E2,  
                   _Input_iterator  
                _Src_first,  
                   _Input_iterator  
                _Src_last,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu))  ;  
  
texture(  
   int                 _E0,  
   unsigned int                 _Bits_per_scalar_element  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   unsigned int                 _Bits_per_scalar_element  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   int                 _E2,  
   unsigned int                 _Bits_per_scalar_element  
) restrict(cpu);  
  
texture(  
   const Concurrency::extent<_Rank>&                 _Ext,  
   unsigned int                 _Bits_per_scalar_element,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   unsigned int                 _Bits_per_scalar_element,  
   const Concurrency::accelerator_view&                 _Av  
)  ;  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   unsigned int                 _Bits_per_scalar_element,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   int                 _E2,  
   unsigned int                 _Bits_per_scalar_element,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
texture(  
   const Concurrency::extent<_Rank>&                 _Ext,  
   _In_ void *                 _Source,  
   unsigned int                 _Src_byte_size,  
   unsigned int                 _Bits_per_scalar_element  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   _In_ void *                 _Source,  
   unsigned int                 _Src_byte_size,  
   unsigned int                 _Bits_per_scalar_element  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   _In_ void *                 _Source,  
   unsigned int                 _Src_byte_size,  
   unsigned int                 _Bits_per_scalar_element  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   int                 _E2,  
   _In_ void *                 _Source,  
   unsigned int                 _Src_byte_size,  
   unsigned int                 _Bits_per_scalar_element  
) restrict(cpu);  
  
texture(  
   const Concurrency::extent<_Rank>&                 _Ext,  
   _In_ void *                 _Source,  
   unsigned int                 _Src_byte_size,  
   unsigned int                 _Bits_per_scalar_element,  
   const Concurrency::accelerator_view&                 _Av  
)  ;  
  
texture(  
   int                 _E0,  
   _In_ void *                 _Source,  
   unsigned int                 _Src_byte_size,  
   unsigned int                 _Bits_per_scalar_element,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   _In_ void *                 _Source,  
   unsigned int                 _Src_byte_size,  
   unsigned int                 _Bits_per_scalar_element,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
texture(  
   int                 _E0,  
   int                 _E1,  
   int                 _E2,  
   _In_ void *                 _Source,  
   unsigned int                 _Src_byte_size,  
   unsigned int                 _Bits_per_scalar_element,  
   const Concurrency::accelerator_view&                 _Av  
) restrict(cpu);  
  
texture(  
   const texture &                 _Src,  
   const Concurrency::accelerator_view &                 _Acc_view  
);  
  
texture(  
   texture &&                 _Other  
);   
  
texture(  
   const Concurrency::extent<                _Rank>& _Ext,   
   unsigned int                 _Bits_per_scalar_element,   
   const Concurrency::accelerator_view& _Av  
);   
  
texture(  
   const texture &                 _Src  
);  
```  
  
### Parameters  
 `_Acc_view`  
 The                                 [accelerator_view](../vs140/accelerator_view-Class.md) that specifies the location of the texture.  
  
 `_Av`  
 The                                 [accelerator_view](../vs140/accelerator_view-Class.md) that specifies the location of the texture.  
  
 `_Associated_av`  
 An accelerator_view that specifies the preferred target for copies to or from this texture.  
  
 `_Bits_per_scalar_element`  
 The number of bits per each scalar element in the underlying scalar type of the texture. In general, supported value are 8, 16, 32, and 64. If 0 is specified, the number of bits is the same as the underlying scalar_type. 64 is only valid for double-based textures.  
  
 `_Ext`  
 The extent in each dimension of the texture.  
  
 `_E0`  
 The most significant component of the texture.  
  
 `_E1`  
 The next-to-most-significant component of the texture.  
  
 `_E2`  
 The least significant component of the extent of the texture.  
  
 `_Input_iterator`  
 The type of the input interator.  
  
 `_Mipmap_levels`  
 The number of mipmap levels in the underlying texture. If 0 is specified, the texture will have the full range of mipmap levels down to the smallest possible size for the specified extent.  
  
 `_Rank`  
 The rank of the extent.  
  
 `_Source`  
 A pointer to a host buffer.  
  
 `_Src`  
 To texture to copy.  
  
 `_Src_byte_size`  
 The number of bytes in the source buffer.  
  
 `_Src_first`  
 A beginning iterator into the source container.  
  
 `_Src_last`  
 An ending iterator into the source container.  
  
 `_Other`  
 Other data source.  
  
 `_Rank`  
 The rank of the section.  
  
## See Also  
 [Concurrency::graphics Namespace](../vs140/Concurrency--graphics-Namespace.md)