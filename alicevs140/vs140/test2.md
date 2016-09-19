---
title: "test2"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0e9a97dd-2f54-490f-8498-23ad7bb80bf3
caps.latest.revision: 29
---
# test2
Describes an object that stores an ordered pair of objects both of type             **double***,* the first representing the real part of a complex number and the second representing the imaginary part.  
  
## Syntax  
  
```  
template<>  
   class complex<double> {  
public:  
   constexpr complex(  
      double             _RealVal = 0,   
      double             _ImagVal = 0  
   );  
  
   constexpr complex(  
      const complex<double>&             _ComplexNum  
   );  
   constexpr explicit complex(  
      const complex<long double>&             _ComplexNum  
   );  
   // rest same as template class complex  
};  
```  
  
#### Parameters  
 `_RealVal`  
 The value of type                         **double** for the real part of the complex number being constructed.  
  
 `_ImagVal`  
 The value of type                         **double** for the imaginary part of the complex number being constructed.  
  
 `_ComplexNum`  
 The complex number of type                         **float** or of type                         `long double` whose real and imaginary parts are used to initialize a complex number of type                         **double** being constructed.  
  
## Return Value  
 A complex number of type                 **double**.  
  
## Remarks  
 The explicit specialization of the template class complex to a complex class of type                 **double** differs from the template class only in the constructors it defines. The conversion from                 **float** to                 **double** is allowed to be implicit, but the conversion from                 `long double` to                 **double** is required to be                 **explicit**. The use of                 **explicit** rules out the initiation with type conversion using assignment syntax.  
  
 For more information on the template class                 `complex`, see                 [complex Class](../vs140/complex-Class.md). For a list of members of the template class                 `complex`, see .  
  
## Example  
  
```  
// complex_comp_dbl.cpp  
// compile with: /EHsc  
#include <complex>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   double pi = 3.14159265359;  
  
   // The first constructor specifies real & imaginary parts  
   complex <double> c1 ( 4.0 , 5.0 );  
   cout << "Specifying initial real & imaginary parts,\n"  
        << " as type double gives c1 = " << c1 << endl;  
  
   // The second constructor initializes values of the real &  
   // imaginary parts using those of complex number of type float  
   complex <float> c2float ( 4.0 , 5.0 );  
   complex <double> c2double ( c2float );  
   cout << "Implicit conversion from type float to type double,"  
        << "\n gives c2double = " << c2double << endl;  
  
   // The third constructor initializes values of the real &  
   // imaginary parts using those of a complex number  
   // of type long double  
   complex <long double> c3longdouble ( 4.0 , 5.0 );  
   complex <double> c3double ( c3longdouble );  
   cout << "Explicit conversion from type float to type double,"  
        << "\n gives c3longdouble = " << c3longdouble << endl;  
  
   // The modulus and argument of a complex number can be recovered  
   double absc3 = abs ( c3longdouble );  
   double argc3 = arg ( c3longdouble );  
   cout << "The modulus of c3 is recovered from c3 using: abs ( c3 ) = "  
        << absc3 << endl;  
   cout << "Argument of c3 is recovered from c3 using:\n arg ( c3 ) = "  
        << argc3 << " radians, which is " << argc3 * 180 / pi  
        << " degrees." << endl;  
}  
/* Output:  
  
Specifying initial real & imaginary parts,  
 as type double gives c1 = (4,5)  
Implicit conversion from type float to type double,  
 gives c2double = (4,5)  
Explicit conversion from type float to type double,  
 gives c3longdouble = (4,5)  
The modulus of c3 is recovered from c3 using: abs ( c3 ) = 6.40312  
Argument of c3 is recovered from c3 using:  
 arg ( c3 ) = 0.896055 radians, which is 51.3402 degrees.*/  
```  
  
## Requirements  
 **Header**: <complex\>  
  
 **Namespace:** std  
  
## See Also  
 [complex Class](../vs140/complex-Class.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)