---
title: "linear_congruential_engine Class"
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
ms.assetid: 30e00ca6-1933-4701-9561-54f3e810a5a1
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# linear_congruential_engine Class
Generates a random sequence by the linear congruential algorithm.  
  
## Syntax  
  
```  
template<class UIntType, UIntType A, UIntType C, UIntType M>  
class linear_congruential_engine{  
public:  
    // types  
    typedef UIntType result_type;  
  
    // engine characteristics  
    static constexpr result_type multiplier = a;  
    static constexpr result_type increment = c;  
    static constexpr result_type modulus = m;  
    static constexpr result_type min() { return c == 0u ? 1u: 0u; }  
    static constexpr result_type max() { return m - 1u; }  
    static constexpr result_type default_seed = 1u;  
  
    // constructors and seeding functions  
    explicit linear_congruential_engine(result_type s = default_seed);  
    template<class Sseq> explicit linear_congruential_engine(Sseq& q);  
    void seed(result_type s = default_seed);  
    template<class Sseq> void seed(Sseq& q);  
  
    // generating functions  
    result_type operator()();  
    void discard(unsigned long long z);  
};  
```  
  
#### Parameters  
 `UIntType`  
 The unsigned integer result type. For possible types, see [<random\>](../vs140/-random-.md).  
  
 `A`  
 **Multiplier**.                         **Precondition**: See Remarks section.  
  
 `C`  
 **Increment**.                         **Precondition**: See Remarks section.  
  
 `M`  
 **Modulus**.                         **Precondition**: See remarks.  
  
## Members  
  
||||  
|-|-|-|  
|`linear_congruential_engine::linear_congruential_engine`|`linear_congruential_engine::min`|`linear_congruential_engine::discard`|  
|`linear_congruential_engine::operator()`|`linear_congruential_engine::max`|`linear_congruential_engine::seed`|  
  
 `default_seed` is a member constant, defined as `1u`, used as the default parameter value for `linear_congruential_engine::seed` and the single value constructor.  
  
 For more information about engine members, see [<random\>](../vs140/-random-.md).  
  
## Remarks  
 The `linear_congruential_engine` template class is the simplest generator engine, but not the fastest or highest quality. An improvement over this engine is the [substract_with_carry_engine](../vs140/subtract_with_carry_engine-Class.md). Neither of these engines is as fast or with as high quality results as the [mersenne_twister_engine](../vs140/mersenne_twister_engine-Class.md).  
  
 This engine produces values of a user-specified unsigned integral type using the recurrence relation ( *period*) `x(i) = (A * x(i-1) + C) mod M`.  
  
 If `M` is zero, the value used for this modulus operation is `numeric_limits<result_type>::max() + 1`. The engine's state is the last value returned, or the seed value if no call has been made to `operator()`.  
  
 If `M` is not zero, the values of the template arguments `A` and `C` must be less than `M`.  
  
 Although you can construct a generator from this engine directly, you can also use one of these predefined typedefs.  
  
 `minstd_rand0`: 1988 minimal standard engine (Lewis, Goodman, and Miller, 1969).  
  
```  
typedef linear_congruential_engine<unsigned int, 16807, 0, 2147483647> minstd_rand0;  
```  
  
 `minstd_rand`: Updated minimal standard engine `minstd_rand0` (Park, Miller, and Stockmeyer, 1993).  
  
```  
typedef linear_congruential_engine<unsigned int, 48271, 0, 2147483647> minstd_rand;  
```  
  
 For detailed information about the linear congruential engine algorithm, see the Wikipedia article                 [Linear congruential generator](http://go.microsoft.com/fwlink/?LinkId=402446).  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
## See Also  
 [<random\>](../vs140/-random-.md)