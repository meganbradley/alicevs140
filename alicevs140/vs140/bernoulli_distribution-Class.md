---
title: "bernoulli_distribution Class"
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
ms.assetid: 586bcde1-95ca-411a-bf17-4aaf19482f34
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# bernoulli_distribution Class
Generates a Bernoulli distribution.  
  
## Syntax  
  
```  
class bernoulli_distribution  
{  
public:  
    // types  
    typedef bool result_type;  
    struct param_type;  
    // constructors and reset functions  
    explicit bernoulli_distribution(double p = 0.5);  
    explicit bernoulli_distribution(const param_type& parm);  
    void reset();  
    // generating functions  
    template<class URNG>  
    result_type operator()(URNG& gen);  
    template<class URNG>  
    result_type operator()(URNG& gen, const param_type& parm);  
    // property functions  
    double p() const;  
    param_type param() const;  
    void param(const param_type& parm);  
    result_type min() const;  
    result_type max() const;  
};  
```  
  
## Remarks  
 The class describes a distribution that produces values of type `bool`, distributed according to the Bernoulli distribution discrete probability function. The following table links to articles about individual members.  
  
||||  
|-|-|-|  
|[bernoulli_distribution::bernoulli_distribution](#bernoulli_distribution__bernoulli_distribution)|`bernoulli_distribution::p`|`bernoulli_distribution::param`|  
|`bernoulli_distribution::operator()`||[bernoulli_distribution::param_type](#bernoulli_distribution__param_type)|  
  
 The property member `p()` returns the currently stored distribution parameter value `p`.  
  
 For more information about distribution classes and their members, see [<random\>](../vs140/-random-.md).  
  
 For detailed information about the Bernoulli distribution discrete probability function, see the Wolfram MathWorld article                 [Bernoulli Distribution](http://go.microsoft.com/fwlink/?LinkId=398467).  
  
## Example  
  
```cpp  
// compile with: /EHsc /W4  
#include <random>   
#include <iostream>  
#include <iomanip>  
#include <string>  
#include <map>  
  
void test(const double p, const int s) {  
  
    // uncomment to use a non-deterministic seed  
    //    std::random_device rd;  
    //    std::mt19937 gen(rd());  
    std::mt19937 gen(1729);  
  
    std::bernoulli_distribution distr(p);  
  
    std::cout << "p == " << distr.p() << std::endl;  
  
    // generate the distribution as a histogram  
    std::map<bool, int> histogram;  
    for (int i = 0; i < s; ++i) {  
        ++histogram[distr(gen)];  
    }  
  
    // print results  
    std::cout << "Histogram for " << s << " samples:" << std::endl;  
    for (const auto& elem : histogram) {  
        std::cout << std::boolalpha << std::setw(5) << elem.first << ' ' << std::string(elem.second, ':') << std::endl;  
    }  
    std::cout << std::endl;  
}  
  
int main()  
{  
    double p_dist = 0.5;  
    int samples = 100;  
  
    std::cout << "Use CTRL-Z to bypass data entry and run using default values." << std::endl;  
    std::cout << "Enter a double value for p distribution (where 0.0 <= p <= 1.0): ";  
    std::cin >> p_dist;  
    std::cout << "Enter an integer value for a sample count: ";  
    std::cin >> samples;  
  
    test(p_dist, samples);  
}  
  
```  
  
## Output  
  
```  
Use CTRL-Z to bypass data entry and run using default values.  
Enter a double value for p distribution (where 0.0 <= p <= 1.0): .45  
Enter an integer value for a sample count: 100  
p == 0.45  
Histogram for 100 samples:  
false :::::::::::::::::::::::::::::::::::::::::::::::::::::  
 true :::::::::::::::::::::::::::::::::::::::::::::::  
```  
  
## Requirements  
 **Header:** <random\>  
  
 **Namespace:** std  
  
##  <a name="bernoulli_distribution__bernoulli_distribution"></a>  bernoulli_distribution::bernoulli_distribution  
 Constructs the distribution.  
  
```  
explicit bernoulli_distribution(double p = 0.5);  
  
explicit bernoulli_distribution(const param_type& parm);  
```  
  
### Parameters  
 `p`  
 The stored `p` distribution parameter.  
  
 `parm`  
 The parameter structure used to construct the distribution.  
  
### Remarks  
 **Precondition:** `0.0 ≤ p ≤ 1.0`  
  
 The first constructor constructs an object whose stored `p` value holds the value `p`.  
  
 The second constructor constructs an object whose stored parameters are initialized from `parm`. You can obtain and set the current parameters of an existing distribution by calling the `param()` member function.  
  
 For more information and a code example, see [bernoulli_distribution Class](../vs140/binomial_distribution-Class.md).  
  
##  <a name="bernoulli_distribution__param_type"></a>  bernoulli_distribution::param_type  
 Contains the parameters of the distribution.  
  
```  
struct param_type {  
    typedef bernoulli_distribution distribution_type;  
    param_type(double p = 0.5);  
    double p() const;  
    .....  
    bool operator==(const param_type& right) const;  
    bool operator!=(const param_type& right) const;  
};  
```  
  
### Parameters  
 See parent topic [bernoulli_distribution Class](../vs140/bernoulli_distribution-Class.md).  
  
### Remarks  
 **Precondition:** `0.0 ≤ p ≤ 1.0`  
  
 This structure can be passed to the distribution's class constructor at instantiation, to the `param()` member function to set the stored parameters of an existing distribution, and to `operator()` to be used in place of the stored parameters.  
  
## See Also  
 [<random\>](../vs140/-random-.md)