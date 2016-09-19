---
title: "atomic_compare"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: efd64570-a666-43bf-96ae-e0e7c9471795
caps.latest.revision: 8
---
# atomic_compare
||||  
|-|-|-|  
|[atomic_compare_exchange_strong](#atomic_compare_exchange_strong)|[atomic_compare_exchange_strong_explicit](#atomic_compare_exchange_strong_explicit)|[atomic_compare_exchange_weak](#atomic_compare_exchange_weak)|  
|[atomic_compare_exchange_weak_explicit](#atomic_compare_exchange_weak_explicit)|[atomic_exchange](#atomic_exchange)|[atomic_exchange_explicit](#atomic_exchange_explicit)|[atomic_fetch_add](#atomic_fetch_add)|  
|[atomic_fetch_add_explicit](#atomic_fetch_add_explicit)|[atomic_fetch_and](#atomic_fetch_and)|[atomic_fetch_and_explicit](#atomic_fetch_and_explicit)|[atomic_fetch_or](#atomic_fetch_or)|  
|[atomic_fetch_or_explicit](#atomic_fetch_or_explicit)|[atomic_fetch_sub](#atomic_fetch_sub)|[atomic_fetch_sub_explicit](#atomic_fetch_sub_explicit)|[atomic_fetch_xor](#atomic_fetch_xor)|  
|[atomic_fetch_xor_explicit](#atomic_fetch_xor_explicit)|[atomic_flag_clear](#atomic_flag_clear)|[atomic_flag_clear_explicit](#atomic_flag_clear_explicit)|[atomic_flag_test_and_set](#atomic_flag_test_and_set)|  
|[atomic_flag_test_and_set_explicit](#atomic_flag_test_and_set_explicit)|[atomic_init](#atomic_init)|[atomic_is_lock_free](#atomic_is_lock_free)|[atomic_load](#atomic_load)|  
|[atomic_load_explicit](#atomic_load_explicit)|[atomic_signal_fence](#atomic_signal_fence)|[atomic_store](#atomic_store)|[atomic_store_explicit](#atomic_store_explicit)|  
|[atomic_thread_fence](#atomic_thread_fence)|[kill_dependency](#kill_dependency)|  
  
##  <a name="atomic_compare_exchange_strong"></a> atomic_compare_exchange_strong  
 Performs an atomic compare and exchange operation.  
  
```  
template <class Ty>  
inline bool atomic_compare_exchange_strong(  
   volatile atomic<                Ty> *                Atom,  
                   Ty *                Exp,  
                   Ty  
                Value  
) _NOEXCEPT;  
template <class Ty>  
inline bool atomic_compare_exchange_strong(  
   atomic<                Ty> *                Atom,  
                   Ty *                Exp,  
                   Ty  
                Value  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `Ty`.  
  
 `Exp`  
 A pointer to a value of type `Ty`.  
  
 `Value`  
 A value of type `Ty`.  
  
### Return Value  
 A                         `bool` that indicates the result of the value comparison.  
  
### Remarks  
 This method performs an atomic compare and exchange operation by using implicit `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) arguments. For more information, see [atomic_compare_exchange_strong_explicit Function](#atomic_compare_exchange_strong_explicit).  
  
##  <a name="atomic_compare_exchange_strong_explicit"></a> atomic_compare_exchange_strong_explicit  
 Performs an *atomic compare and exchange* operation.  
  
```  
template <class _Ty>  
inline bool atomic_compare_exchange_strong_explicit(  
   volatile atomic<                Ty> *                Atom,  
                   Ty *                Exp,  
                   Ty  
                Value,  
   memory_order Order1,  
   memory_order Order2  
) _NOEXCEPT;  
  
template <class Ty>  
inline bool atomic_compare_exchange_strong_explicit(  
   atomic<                Ty> *                Atom,  
                   Ty *                Exp,  
                   Ty  
                Value,  
   memory_order Order1,  
   memory_order Order2  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `Ty`.  
  
 `Exp`  
 A pointer to a value of type `Ty`.  
  
 `Value`  
 A value of type `Ty`.  
  
 `Order1`  
 First [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) argument.  
  
 `Order2`  
 Second `memory_order` argument. The value of `Order2` cannot be `memory_order_release` or `memory_order_acq_rel`, it cannot be stronger than the value of `Order1`.  
  
### Return Value  
 A                         `bool` that indicates the result of the value comparison.  
  
### Remarks  
 An *atomic compare and exchange operation* compares the value that is stored in the object that is pointed to by `Atom` against the value that is pointed to by `Exp`. If the values are equal, the the value that is stored in the object that is pointed to by `atom` is replaced with `Val` by using a `read-modify-write` operation and applying the memory order constraints that are specified by `Order1`. If the values are not equal, the operation replaces the value that is pointed to by `Exp` with the value that is stored in the object that is pointed to by `Atom` and applies the memory order constraints that are specified by `Order2`.  
  
##  <a name="atomic_compare_exchange_weak"></a> atomic_compare_exchange_weak  
 Performs a *weak atomic compare and exchange* operation.  
  
```  
template <class Ty>  
inline bool atomic_compare_exchange_strong(  
   volatile atomic<                Ty> *                Atom,  
                   Ty *                Exp,  
                   Ty  
                Value  
) _NOEXCEPT;  
template <class Ty>  
inline bool atomic_compare_exchange_strong(  
   atomic<                Ty> *                Atom,  
                   Ty *                Exp,  
                   Ty  
                Value  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `Ty`.  
  
 `Exp`  
 A pointer to a value of type `Ty`.  
  
 `Value`  
 A value of type `Ty`.  
  
### Return Value  
 A                         `bool` that indicates the result of the value comparison.  
  
### Remarks  
 This method performs a *weak atomic compare and exchange operation* that has implicit `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) arguments. For more information, see [atomic_compare_exchange_weak_explicit Function](#atomic_compare_exchange_weak_explicit).  
  
##  <a name="atomic_compare_exchange_weak_explicit"></a> atomic_compare_exchange_weak_explicit  
 Performs a *weak atomic compare and exchange* operation.  
  
```  
template <class Ty>  
inline bool atomic_compare_exchange_weak_explicit(  
   volatile atomic<                Ty> *                Atom,  
                   Ty *                Exp,  
                   Ty  
                Value,  
   memory_order Order1,  
   memory_order Order2  
) _NOEXCEPT;  
template <class Ty>  
inline bool atomic_compare_exchange_weak_explicit(  
   atomic<                Ty> *                Atom,  
                   Ty *                Exp,  
                   Ty  
                Value,  
   memory_order Order1,  
   memory_order Order2  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `Ty`.  
  
 `Exp`  
 A pointer to a value of type `Ty`.  
  
 `Value`  
 A value of type `Ty`.  
  
 `Order1`  
 First [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) argument.  
  
 `Order2`  
 Second `memory_order` argument. The value of `Order2` cannot be `memory_order_release` or `memory_order_acq_rel`, nor can it be stronger than the value of `Order1`.  
  
### Return Value  
 A                         `bool` that indicates the result of the value comparison.  
  
### Remarks  
 An *atomic compare and exchange operation* compares the value that is stored in the object that is pointed to by `Atom` with the value that is pointed to by `Exp`. If the values are equal, the operation replaces the value that is stored in the object that is pointed to by `Atom` with `Val` by using a `read-modify-write` operation and applying the memory-order constraints that are specified by `Order1`. If the values are not equal, the operation replaces the value that is pointed to by `Exp` with the value that is stored in the object that is pointed to by `Atom` and applies the memory-order constraints that are specified by `Order2`.  
  
 A                         *weak* atomic compare and exchange operation performs an exchange if the compared values are equal. However, if the values are not equal, the operation is not guaranteed to perform an exchange.  
  
##  <a name="atomic_exchange"></a> atomic_exchange  
 Uses `Value` to replace the stored value of `Atom`.  
  
```  
template <class _Ty>  
inline Ty atomic_exchange(  
   volatile atomic<                Ty> *                _Atom,  
                   Ty  
                Value  
) _NOEXCEPT;  
template <class Ty>  
inline _Ty atomic_exchange(  
   atomic<                Ty> *                Atom,  
                   Ty  
                Value  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `Ty`.  
  
 `Value`  
 A value of type `Ty`.  
  
### Return Value  
 The stored value of `Atom` before the exchange.  
  
### Remarks  
 The `atomic_exchange` function performs a `read-modify-write` operation to exchange the value that is stored in `Atom` with `Value`, using the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
##  <a name="atomic_exchange_explicit"></a> atomic_exchange_explicit  
 Replaces the stored value of `Atom` with `Value`.  
  
```  
template <class Ty>  
inline Ty atomic_exchange_explicit(  
   volatile atomic<                Ty> *                Atom,  
                   Ty  
                Value,  
   memory_order Order  
) _NOEXCEPT;  
template <class Ty>  
inline Ty atomic_exchange_explicit(  
   atomic<                Ty> *                Atom,  
                   Ty  
                Value,  
   memory_order Order  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `Ty`.  
  
 `Value`  
 A value of type `Ty`.  
  
 `Order`  
 A                                 [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
### Return Value  
 The stored value of `Atom` before the exchange.  
  
### Remarks  
 The `atomic_exchange_explicit` function performs a `read-modify-write` operation to exchange the value that is stored in `Atom` with `Value`, within the memory constraints that are specified by `Order`.  
  
##  <a name="atomic_fetch_add"></a> atomic_fetch_add  
 Adds a value to an existing value that is stored in an `atomic` object.  
  
```  
template <class T>                 T* atomic_fetch_add(  
   volatile atomic<                T*> *                Atom,  
   ptrdiff_t Value  
) noexcept;  
  
template <class T>                 T* atomic_fetch_add(  
   atomic<                T*> *                Atom,  
   ptrdiff_t Value  
) noexcept;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a pointer to type `T`.  
  
 `Value`  
 A value of type `ptrdiff_t`.  
  
### Return Value  
 The value of the pointer contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_add` function performs a `read-modify-write` operation to atomically add `Value` to the stored value in `Atom`, using the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraint.  
  
 When the atomic type is `atomic_address`,                         `Value` has type `ptrdiff_t` and the operation treats the stored pointer as a `char *`.  
  
 This operation is also overloaded for integral types:  
  
```cpp  
integral atomic_fetch_add(  
    volatile atomic-integral * Atom, integral Value  
) noexcept;  
  
integral atomic_fetch_add(  
    atomic-integral * Atom, integral Value  
) noexcept;  
```  
  
##  <a name="atomic_fetch_add_explicit"></a> atomic_fetch_add_explicit  
 Adds a value to an existing value that is stored in an `atomic` object.  
  
```  
template <class T>                 T* atomic_fetch_add_explicit(  
   volatile atomic<                T*> *                Atom,  
   ptrdiff_t Value,  
   memory_order Order  
) noexcept;  
  
template <class T>                 T* atomic_fetch_add_explicit(  
   atomic<                T*> *                Atom,  
   ptrdiff_t Value,   memory_order Order  
) noexcept;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a pointer to type `T`.  
  
 `Value`  
 A value of type `ptrdiff_t`.  
  
### Return Value  
 The value of the pointer contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_add_explicit` function performs a `read-modify-write` operation to atomically add `Value` to the stored value in `Atom`, within the [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraints that are specified by `Order`.  
  
 When the atomic type is `atomic_address`,                         `Value` has type `ptrdiff_t` and the operation treats the stored pointer as a `char *`.  
  
 This operation is also overloaded for integral types:  
  
```cpp  
integral atomic_fetch_add_explicit(  
    volatile atomic-integral * Atom, integral Value, memory_order Order  
) noexcept;  
  
integral atomic_fetch_add_explicit(  
    atomic-integral * Atom, integral Value, memory_order Order  
) noexcept;  
```  
  
##  <a name="atomic_fetch_and"></a> atomic_fetch_and  
 Performs a bitwise `and` on a value and an existing value that is stored in an `atomic` object.  
  
```  
template <class T>  
inline T atomic_fetch_and(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value); noexcept  
template <class T>  
inline T atomic_fetch_and(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value); noexcept  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `T`.  
  
 `Value`  
 A value of type `T`.  
  
### Return Value  
 The value contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_and` function performs a `read-modify-write` operation to replace the stored value of `Atom` with a bitwise `and` of `Value` and the current value that is stored in `Atom`, using the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraint.  
  
##  <a name="atomic_fetch_and_explicit"></a> atomic_fetch_and_explicit  
 Performs a bitwise `and` of a value and an existing value that is stored in an `atomic` object.  
  
```  
template <class T>  
inline T atomic_fetch_and_explicit(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value,  
   memory_order Order); noexcepttemplate <class T>  
inline T atomic_fetch_and_explicit(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value,  
   memory_order Order); noexcept  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `T`.  
  
 `Value`  
 A value of type `T`.  
  
 `Order`  
 A                                 [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
### Return Value  
 The value contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_and_explicit` function performs a `read-modify-write` operation to replace the stored value of `Atom` with a bitwise `and` of `Value` and the current value that is stored in `Atom`, within the memory constraints that are specified by `Order`.  
  
##  <a name="atomic_fetch_or"></a> atomic_fetch_or  
 Performs a bitwise `or` on a value and an existing value that is stored in an `atomic` object.  
  
```  
template <class T>  
inline T atomic_fetch_or (  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value); noexcept  
template <class T>  
inline T atomic_fetch_or (  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value); noexcept  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `T`.  
  
 `Value`  
 A value of type `T`.  
  
### Return Value  
 The value contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_or` function performs a `read-modify-write` operation to replace the stored value of `Atom` with a bitwise `or` of `Value` and the current value that is stored in `Atom`, using the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
##  <a name="atomic_fetch_or_explicit"></a> atomic_fetch_or_explicit  
 Performs a bitwise `or` on a value and an existing value that is stored in an `atomic` object.  
  
```  
template <class T>  
inline T atomic_fetch_or_explicit(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value,  
   memory_order Order); noexcepttemplate <class T>  
inline T atomic_fetch_or_explicit(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value,  
   memory_order Order); noexcept  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `T`.  
  
 `Value`  
 A value of type `T`.  
  
 `Order`  
 A                                 [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
### Return Value  
 The value contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_or_explicit` function performs a `read-modify-write` operation to replace the stored value of `Atom` with a bitwise `or` of `Value` and the current value that is stored in `Atom`, within the [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraints specified by `Order`.  
  
##  <a name="atomic_fetch_sub"></a> atomic_fetch_sub  
 Subtracts a value from an existing value that is stored in an `atomic` object.  
  
```  
template <class T>                 T* atomic_fetch_sub(  
   volatile atomic<                T*> *                Atom,  
   ptrdiff_t Value  
) noexcept;  
  
template <class T>                 T* atomic_fetch_sub(  
   atomic<                T*> *                Atom,  
   ptrdiff_t Value  
) noexcept;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a pointer to type `T`.  
  
 `Value`  
 A value of type `ptrdiff_t`.  
  
### Return Value  
 The value of the pointer contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_sub` function performs a `read-modify-write` operation to atomically subtract `Value` from the stored value in `Atom`, using the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraint.  
  
 When the atomic type is `atomic_address`,                         `Value` has type `ptrdiff_t` and the operation treats the stored pointer as a `char *`.  
  
 This operation is also overloaded for integral types:  
  
```cpp  
integral atomic_fetch_sub(  
    volatile atomic-integral * Atom, integral Value  
) noexcept;  
  
integral atomic_fetch_sub(  
    atomic-integral * Atom, integral Value  
) noexcept;  
```  
  
##  <a name="atomic_fetch_sub_explicit"></a> atomic_fetch_sub_explicit  
 Subtracts a value from an existing value that is stored in an `atomic` object.  
  
```  
template <class T>                 T* atomic_fetch_sub_explicit(  
   volatile atomic<                T*> *                Atom,  
   ptrdiff_t Value,  
   memory_order Order  
) noexcept;  
  
template <class T>                 T* atomic_fetch_sub_explicit(  
   atomic<                T*> *                Atom,  
   ptrdiff_t Value,   memory_order Order  
) noexcept;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a pointer to type `T`.  
  
 `Value`  
 A value of type `ptrdiff_t`.  
  
### Return Value  
 The value of the pointer contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_sub_explicit` function performs a `read-modify-write` operation to atomically subtract `Value` from the stored value in `Atom`, within the [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraints that are specified by `Order`.  
  
 When the atomic type is `atomic_address`,                         `Value` has type `ptrdiff_t` and the operation treats the stored pointer as a `char *`.  
  
 This operation is also overloaded for integral types:  
  
```cpp  
integral atomic_fetch_sub_explicit(  
    volatile atomic-integral * Atom, integral Value, memory_order Order  
) noexcept;  
  
integral atomic_fetch_sub_explicit(  
    atomic-integral * Atom, integral Value, memory_order Order  
) noexcept;  
```  
  
##  <a name="atomic_fetch_xor"></a> atomic_fetch_xor  
 Performs a bitwise `exclusive or` on a value and an existing value that is stored in an `atomic` object.  
  
```  
template <class T>  
inline T atomic_fetch_xor(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value); noexcept  
  
template <class T>  
inline T atomic_fetch_xor(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value); noexcept  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `T`.  
  
 `Value`  
 A value of type `T`.  
  
### Return Value  
 The value contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_xor` function performs a `read-modify-write` operation to replace the stored value of `Atom` with a bitwise `exclusive or` of `Value` and the current value that is stored in `Atom`, using the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
##  <a name="atomic_fetch_xor_explicit"></a> atomic_fetch_xor_explicit  
 Performs a bitwise `exclusive or` on a value and an existing value that is stored in an `atomic` object.  
  
```  
template <class T>  
inline T atomic_fetch_xor_explicit(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value,  
   memory_order Order); noexcepttemplate <class T>  
inline T atomic_fetch_xor_explicit(  
   volatile atomic<                T>*                 Atom,  
                   T  
                Value,  
   memory_order Order); noexcept  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `T`.  
  
 `Value`  
 A value of type `T`.  
  
 `Order`  
 A                                 [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
### Return Value  
 The value contained by the atomic object immediately before the operation was performed.  
  
### Remarks  
 The `atomic_fetch_xor_explicit` function performs a `read-modify-write` operation to replace the stored value of `Atom` with a bitwise `exclusive or` of `Value` and the current value that is stored in `Atom`, within the [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraints that are specified by `Order`.  
  
##  <a name="atomic_flag_clear"></a> atomic_flag_clear  
 Sets the `bool` flag in an [atomic_flag](../vs140/atomic_flag-Structure.md) object to `false`, within the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
```  
inline void atomic_flag_clear(  
   volatile atomic_flag *                Flag  
) _NOEXCEPT;  
inline void atomic_flag_clear(  
   atomic_flag *                Flag  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Flag`  
 A pointer to an `atomic_flag` object.  
  
##  <a name="atomic_flag_clear_explicit"></a> atomic_flag_clear_explicit  
 Sets the `bool` flag in an [atomic_flag](../vs140/atomic_flag-Structure.md) object to `false`, within the specified [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraints.  
  
```  
inline void atomic_flag_clear_explicit(  
   volatile atomic_flag *                Flag,  
   memory_order Order  
) _NOEXCEPT;  
inline void atomic_flag_clear_explicit(  
   atomic_flag *                Flag,  
   memory_order Order  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Flag`  
 A pointer to an `atomic_flag` object.  
  
 `Order`  
 A                                 [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
##  <a name="atomic_flag_test_and_set"></a> atomic_flag_test_and_set  
 Sets the `bool` flag in an [atomic_flag](../vs140/atomic_flag-Structure.md) object to `true`, within the constraints of the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
```  
inline bool atomic_flag_test_and_set(  
   volatile atomic_flag *                Flag,  
) _NOEXCEPT;  
inline bool atomic_flag_test_and_set(  
   atomic_flag *                Flag,  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Flag`  
 A pointer to an `atomic_flag` object.  
  
### Return Value  
 The initial value of `Flag`.  
  
##  <a name="atomic_flag_test_and_set_explicit"></a> atomic_flag_test_and_set_explicit  
 Sets the `bool` flag in an [atomic_flag](../vs140/atomic_flag-Structure.md) object to `true`, within the specified [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraints.  
  
```  
inline bool atomic_flag_test_and_set_explicit(  
   volatile atomic_flag *                Flag,  
   memory_order Order  
) _NOEXCEPT;  
inline bool atomic_flag_test_and_set_explicit(  
   atomic_flag *                Flag,  
   memory_order Order  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Flag`  
 A pointer to an `atomic_flag` object.  
  
 `Order`  
 A                                 [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
### Return Value  
 The initial value of `Flag`.  
  
##  <a name="atomic_init"></a> atomic_init  
 Sets the stored value in an `atomic` object.  
  
```  
template <class Ty>  
inline void atomic_init(  
   volatile atomic<                Ty> *                Atom,  
                   Ty  
                Value  
) _NOEXCEPT;  
template <class Ty>  
inline void atomic_init(  
   atomic<                Ty> *                Atom,  
                   Ty  
                Value  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `Ty`.  
  
 `Value`  
 A value of type `Ty`.  
  
### Remarks  
 `atomic_init` is not an atomic operation. It is not thread-safe.  
  
##  <a name="atomic_is_lock_free"></a> atomic_is_lock_free  
 Specifies whether atomic operations on an `atomic` object are *lock-free*.  
  
```  
template <class T>  
inline bool atomic_is_lock_free(  
   const volatile atomic<                T> *                Atom  
) _NOEXCEPT;  
template <class T>  
inline bool atomic_is_lock_free(  
   const atomic<                T> *                Atom  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `T`.  
  
### Return Value  
 `true` if atomic operations on `Atom` are lock-free; otherwise,                         `false`.  
  
### Remarks  
 An atomic type is lock-free if no atomic operations on that type use locks. If this function returns true, the type is safe to use in signal-handlers.  
  
##  <a name="atomic_load"></a> atomic_load  
 Retrieves the stored value in an `atomic` object.  
  
```  
template <class Ty>  
inline Ty atomic_load(  
   const volatile atomic<                Ty> *                Atom) _NOEXCEPT;  
template <class Ty>  
inline Ty atomic_load(  
   const atomic<                Ty> *                Atom) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that contains a value of type `Ty`.  
  
### Return Value  
 The retrieved value that is stored in `Atom`.  
  
### Remarks  
 `atomic_load` implicitly uses the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
##  <a name="atomic_load_explicit"></a> atomic_load_explicit  
 Retrieves the stored value in an `atomic` object, within a specified [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum).  
  
```  
template <class Ty>  
inline Ty atomic_load_explicit(  
   const volatile atomic<                Ty> *                Atom,  
   memory_order Order  
) _NOEXCEPT;  
template <class Ty>  
inline Ty atomic_load_explicit(  
   const atomic<                Ty> *                Atom,  
   memory_order Order  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that contains a value of type `Ty`.  
  
 `Order`  
 A                                 [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum). Do not use `memory_order_release` or `memory_order_acq_rel`.  
  
### Return Value  
 The retrieved value that is stored in `Atom`.  
  
##  <a name="atomic_signal_fence"></a> atomic_signal_fence  
 Acts as a *fence*â€”which is a memory synchronization primitive that enforces ordering between load/store operationsâ€”between other fences in a calling thread that have signal handlers that are executed in the same thread.  
  
```  
inline void atomic_signal_fence(  
   memory_order Order  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Order`  
 A memory ordering constraint that determines fence type.  
  
### Remarks  
 The `Order` argument determines fence type.  
  
|||  
|-|-|  
|`memory_order_relaxed`|The fence has no effect.|  
|`memory_order_consume`|The fence is an acquire fence.|  
|`memory_order_acquire`|The fence is an acquire fence.|  
|`memory_order_release`|The fence is a release fence.|  
|`memory_order_acq_rel`|The fence is both an acquire fence and a release fence.|  
|`memory_order_seq_cst`|The fence is both an acquire fence and a release fence, and is sequentially consistent.|  
  
##  <a name="atomic_store"></a> atomic_store  
 Atomically stores a value in an atomic object.  
  
```  
template <class Ty>  
inline Ty atomic_store_explicit(  
   const volatile atomic<                Ty> *                Atom,  
                   Ty  
                Value  
) _NOEXCEPT;  
template <class Ty>  
inline Ty atomic_store_explicit(  
   const atomic<                Ty> *                Atom,  
                   _Ty  
                Value  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an atomic object that contains a value of type `Ty`.  
  
 `Value`  
 A value of type `Ty`.  
  
### Remarks  
 `atomic_store` stores `Value` in the object that is pointed to by `Atom`, within the `memory_order_seq_cst`[memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum) constraint.  
  
##  <a name="atomic_store_explicit"></a> atomic_store_explicit  
 Atomically stores a value in an atomic object.  
  
```  
template <class Ty>  
inline Ty atomic_store_explicit(  
   const volatile atomic<                Ty> *                Atom,                   Ty  
                Value,  
   memory_order Order  
) _NOEXCEPT;  
template <class Ty>  
inline Ty atomic_store_explicit(  
   const atomic<                Ty> *                Atom,  
                   _Ty  
                Value,  
   memory_order Order  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Atom`  
 A pointer to an `atomic` object that contains a value of type `Ty`.  
  
 `Value`  
 A value of type `Ty`.  
  
 `Order`  
 A                                 [memory_order](../vs140/memory_order-Enum.md#memory_order%20Enum). Do not use `memory_order_consume`,                                 `memory_order_acquire`, or `memory_order_acq_rel`.  
  
### Remarks  
 `atomic_store` stores `Value` in the object that is pointed to by `Atom`, within the `memory_order` that is specified by `Order`.  
  
##  <a name="atomic_thread_fence"></a> atomic_thread_fence  
 Acts as a *fence*â€”which is a memory synchronization primitive that enforces ordering between load/store operationsâ€”without an associated atomic operation.  
  
```  
inline void atomic_thread_fence(  
   memory_order Order  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Order`  
 A memory ordering constraint that determines fence type.  
  
### Remarks  
 The `Order` argument determines fence type.  
  
|||  
|-|-|  
|`memory_order_relaxed`|The fence has no effect.|  
|`memory_order_consume`|The fence is an acquire fence.|  
|`memory_order_acquire`|The fence is an acquire fence.|  
|`memory_order_release`|The fence is a release fence.|  
|`memory_order_acq_rel`|The fence is both an acquire fence and a release fence.|  
|`memory_order_seq_cst`|The fence is both an acquire fence and a release fence, and is sequentially consistent.|  
  
##  <a name="kill_dependency"></a> kill_dependency  
 Removes a dependency.  
  
```  
template<class Ty>  
Ty kill_dependency(  
                   Ty  
                Arg  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Arg`  
 A value of type `Ty`.  
  
### Return Value  
 The return value is `Arg`. The evaluation of `Arg` does not carry a dependency to the function call. By breaking a possible dependency chain, the function might permit the compiler to generate more efficient code.