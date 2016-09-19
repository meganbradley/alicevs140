---
title: "Outline of Changes (C++-CLI)"
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
H1: Outline of Changes (C++/CLI)
ms.assetid: c0bbbd6b-c5c4-44cf-a6ca-c1010c377e9d
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Outline of Changes (C++-CLI)
This outline shows you examples of some of the changes in the language from Managed Extensions for C++ to [!INCLUDE[cpp_current_long](../vs140/includes/cpp_current_long_md.md)]. Follow the link that accompanies each item for more information.  
  
## No Double Underscore Keywords  
 The double underscore in front of all keywords has been removed, with one exception. Thus, `__value` becomes `value`, and `__interface` becomes `interface`, and so on. To prevent name clashes between keywords and identifiers in user code, keywords are primarily treated as contextual.  
  
 See [Language Keywords](../vs140/Language-Keywords--C---CLI-.md) for more information.  
  
## Class Declarations  
 Managed Extensions syntax:  
  
```  
__gc class Block {};                           // reference class  
__value class Vector {};                       // value class  
__interface I {};                        // interface class  
__gc __abstract class Shape {};                // abstract class  
__gc __sealed class Shape2D : public Shape {}; // derived class  
```  
  
 New syntax:  
  
```  
ref class Block {};                // reference class  
value class Vector {};             // value class  
interface class I {};        // interface class  
ref class Shape abstract {};       // abstract class  
ref class Shape2D sealed: Shape{}; // derived class  
```  
  
 See [The Managed Types](../vs140/Managed-Types--C---CL-.md) for more information.  
  
## Object Declaration  
 Managed Extensions syntax:  
  
```  
public __gc class Form1 : public System::Windows::Forms::Form {  
private:  
   System::ComponentModel::Container __gc *components;  
   System::Windows::Forms::Button   __gc *button1;  
   System::Windows::Forms::DataGrid __gc *myDataGrid;     
   System::Data::DataSet  __gc *myDataSet;  
};  
```  
  
 New syntax:  
  
```  
public ref class Form1 : System::Windows::Forms::Form {  
   System::ComponentModel::Container^ components;  
   System::Windows::Forms::Button^ button1;  
   System::Windows::Forms::DataGrid^ myDataGrid;  
   System::Data::DataSet^ myDataSet;  
};  
```  
  
 See [Declaration of a CLR Reference Class Object](../vs140/Declaration-of-a-CLR-Reference-Class-Object.md) for more information.  
  
### Managed Heap Allocation  
 Managed Extensions syntax:  
  
```  
Button* button1 = new Button; // managed heap  
int *pi1 = new int;           // native heap  
Int32 *pi2 = new Int32;       // managed heap  
```  
  
 New syntax:  
  
```  
Button^ button1 = gcnew Button;        // managed heap  
int * pi1 = new int;                   // native heap  
Int32^ pi2 = gcnew Int32;              // managed heap  
```  
  
 See [Declaration of a CLR Reference Class Object](../vs140/Declaration-of-a-CLR-Reference-Class-Object.md) for more information.  
  
### A Tracking Reference to No Object  
 Managed Extensions syntax:  
  
```  
// OK: we set obj to refer to no object  
Object * obj = 0;  
  
// Error: no implicit boxing  
Object * obj2 = 1;  
```  
  
 New syntax:  
  
```  
// Incorrect Translation  
// causes the implicit boxing of both 0 and 1  
Object ^ obj = 0;  
Object ^ obj2 = 1;  
  
// Correct Translation  
// OK: we set obj to refer to no object  
Object ^ obj = nullptr;  
  
// OK: we initialize obj2 to an Int32^  
Object ^ obj2 = 1;  
```  
  
 See [Declaration of a CLR Reference Class Object](../vs140/Declaration-of-a-CLR-Reference-Class-Object.md) for more information.  
  
## Array Declaration  
 The CLR array has been redesigned. It is similar to the stl `vector` template collection, but maps to the underlying `System::Array` class – that is, it is not a template implementation.  
  
 See [Declaration of a CLR Array](../vs140/Declaration-of-a-CLR-Array.md) for more information.  
  
### Array as Parameter  
 Managed Extensions array syntax:  
  
```  
void PrintValues( Object* myArr __gc[]);   
void PrintValues( int myArr __gc[,,]);   
```  
  
 New array syntax:  
  
```  
void PrintValues( array<Object^>^ myArr );  
void PrintValues( array<int,3>^ myArr );  
```  
  
### Array as Return Type  
 Managed Extensions array syntax:  
  
```  
Int32 f() [];   
int GetArray() __gc[];  
```  
  
 New array syntax:  
  
```  
array<Int32>^ f();  
array<int>^ GetArray();  
```  
  
### Shorthand Initialization of Local CLR Array  
 Managed Extensions array syntax:  
  
```  
int GetArray() __gc[] {  
   int a1 __gc[] = { 1, 2, 3, 4, 5 };  
   Object* myObjArray __gc[] = { __box(26), __box(27), __box(28),  
                                 __box(29), __box(30) };  
  
   return a1;  
}  
```  
  
 New array syntax:  
  
```  
array<int>^ GetArray() {  
   array<int>^ a1 = {1,2,3,4,5};  
   array<Object^>^ myObjArray = {26,27,28,29,30};  
  
   return a1;  
}  
```  
  
### Explicit CLR Array Declaration  
 Managed Extensions array syntax:  
  
```  
Object* myArray[] = new Object*[2];  
String* myMat[,] = new String*[4,4];  
```  
  
 New array syntax:  
  
```  
array<Object^>^ myArray = gcnew array<Object^>(2);  
array<String^,2>^ myMat = gcnew array<String^,2>(4,4);  
```  
  
 New to language: explicit array initialization that follows gcnew  
  
```  
// explicit initialization list follow gcnew   
// is not supported in Managed Extensions  
array<Object^>^ myArray =   
   gcnew array<Object^>(4){ 1, 1, 2, 3 };  
```  
  
## Scalar Properties  
 Managed Extensions property syntax:  
  
```  
public __gc __sealed class Vector {  
   double _x;  
  
public:  
   __property double get_x(){ return _x; }  
   __property void set_x( double newx ){ _x = newx; }  
};  
```  
  
 New property syntax:  
  
```  
public ref class Vector sealed {   
   double _x;  
  
public:  
   property double x   
   {  
      double get()             { return _x; }  
      void   set( double newx ){ _x = newx; }  
   } // Note: no semi-colon …  
};  
```  
  
 New to language: trivial properties  
  
```  
public ref class Vector sealed {   
public:  
   // equivalent shorthand property syntax  
   // backing store is not accessible  
   property double x;   
};  
```  
  
 See [Property Declaration](../vs140/Property-Declaration.md) for more information.  
  
## Indexed Properties  
 Managed Extensions indexed property syntax:  
  
```  
public __gc class Matrix {  
   float mat[,];  
  
public:   
   __property void set_Item( int r, int c, float value) { mat[r,c] = value; }  
   __property int get_Item( int r, int c ) { return mat[r,c]; }  
};  
```  
  
 New indexed property syntax:  
  
```  
public ref class Matrix {  
   array<float, 2>^ mat;  
  
public:  
   property float Item [int,int] {  
      float get( int r, int c ) { return mat[r,c]; }  
      void set( int r, int c, float value ) { mat[r,c] = value; }  
   }  
};  
```  
  
 New to language: class-level indexed property  
  
```  
public ref class Matrix {  
   array<float, 2>^ mat;  
  
public:  
   // ok: class level indexer now  
   //     Matrix mat;  
   //     mat[ 0, 0 ] = 1;   
   //  
   // invokes the set accessor of the default indexer  
  
   property float default [int,int] {  
      float get( int r, int c ) { return mat[r,c]; }  
      void set( int r, int c, float value ) { mat[r,c] = value; }  
   }  
};  
```  
  
 See [Property Index Declaration](../vs140/Property-Index-Declaration.md) for more information.  
  
## Overloaded Operators  
 Managed Extensions operator overload syntax:  
  
```  
public __gc __sealed class Vector {  
public:  
   Vector( double x, double y, double z );  
  
   static bool    op_Equality( const Vector*, const Vector* );  
   static Vector* op_Division( const Vector*, double );  
};  
  
int main() {  
   Vector *pa = new Vector( 0.231, 2.4745, 0.023 );  
   Vector *pb = new Vector( 1.475, 4.8916, -1.23 );   
  
   Vector *pc = Vector::op_Division( pa, 4.8916 );  
  
   if ( Vector::op_Equality( pa, pc ))  
      ;  
}  
```  
  
 New operator overload syntax:  
  
```  
public ref class Vector sealed {  
public:  
   Vector( double x, double y, double z );  
  
   static bool    operator ==( const Vector^, const Vector^ );  
   static Vector^ operator /( const Vector^, double );  
};  
  
int main() {  
   Vector^ pa = gcnew Vector( 0.231, 2.4745, 0.023 );  
   Vector^ pb = gcnew Vector( 1.475, 4.8916, -1.23 );  
  
   Vector^ pc = pa / 4.8916;  
   if ( pc == pa )  
      ;  
}  
```  
  
 See [Overloaded Operators](../vs140/Overloaded-Operators.md) for more information.  
  
## Conversion Operators  
 Managed Extensions conversion operator syntax:  
  
```  
__gc struct MyDouble {  
   static MyDouble* op_Implicit( int i );   
   static int op_Explicit( MyDouble* val );  
   static String* op_Explicit( MyDouble* val );   
};  
```  
  
 New conversion operator syntax:  
  
```  
ref struct MyDouble {  
public:  
   static operator MyDouble^ ( int i );  
   static explicit operator int ( MyDouble^ val );  
   static explicit operator String^ ( MyDouble^ val );  
};  
```  
  
 See [Changes to Conversion Operators](../vs140/Changes-to-Conversion-Operators.md) for more information.  
  
## Explicit Override of an Interface Member  
 Managed Extensions explicit override syntax:  
  
```  
public __gc class R : public ICloneable {  
   // to be used through ICloneable  
   Object* ICloneable::Clone();  
  
   // to be used through an R  
   R* Clone();  
};  
```  
  
 New explicit override syntax:  
  
```  
public ref class R : public ICloneable {  
   // to be used through ICloneable  
   virtual Object^ InterfaceClone() = ICloneable::Clone;  
  
   // to be used through an R   
   virtual R^ Clone();  
};  
```  
  
 See [Explicit Override of an Interface Member](../vs140/Explicit-Override-of-an-Interface-Member.md) for more information.  
  
## Private Virtual Functions  
 Managed Extensions private virtual function syntax:  
  
```  
__gc class Base {  
private:  
   // inaccessible to a derived class  
   virtual void g();   
};  
  
__gc class Derived : public Base {  
public:  
   // ok: g() overrides Base::g()  
   virtual void g();  
};  
```  
  
 New private virtual function syntax  
  
```  
ref class Base {  
private:  
   // inaccessible to a derived class  
   virtual void g();   
};  
  
ref class Derived : public Base {  
public:  
   // error: cannot override: Base::g() is inaccessible  
   virtual void g() override;  
};  
```  
  
 See [Private Virtual Functions](../vs140/Private-Virtual-Functions.md) for more information.  
  
## CLR Enum Type  
 Managed Extensions enum syntax:  
  
```  
__value enum e1 { fail, pass };  
public __value enum e2 : unsigned short  {   
   not_ok = 1024,   
   maybe, ok = 2048   
};    
```  
  
 New enum syntax:  
  
```  
enum class e1 { fail, pass };  
public enum class e2 : unsigned short {   
   not_ok = 1024,  
   maybe, ok = 2048   
};  
```  
  
 Apart from this small syntactic change, the behavior of the CLR enum type has been changed in a number of ways:  
  
-   A forward declaration of a CLR enum is no longer supported.  
  
-   The overload resolution between the built-in arithmetic types and the Object class hierarchy has reversed between Managed Extensions and [!INCLUDE[cpp_current_long](../vs140/includes/cpp_current_long_md.md)]. As a side-effect, CLR enums are no longer implicitly converted to arithmetic types.  
  
-   In the new syntax, a CLR enum maintains its own scope, which is not the case in Managed Extensions. Previously, enumerators were visible within the containing scope of the enum; now, enumerators are encapsulated within the scope of the enum.  
  
 See [CLR Enum Type](../vs140/CLR-Enum-Type.md) for more information.  
  
## Removal of __box Keyword  
 Managed Extensions boxing syntax:  
  
```  
Object *o = __box( 1024 ); // explicit boxing  
```  
  
 New boxing syntax:  
  
```  
Object ^o = 1024; // implicit boxing  
```  
  
 See [A Tracking Handle to a Boxed Value](../vs140/A-Tracking-Handle-to-a-Boxed-Value.md) for more information.  
  
## Pinning Pointer  
 Managed Extensions pinning pointer syntax:  
  
```  
__gc struct H { int j; };  
  
int main() {  
   H * h = new H;  
   int __pin * k = & h -> j;  
};  
```  
  
 New pinning pointer syntax:  
  
```  
ref struct H { int j; };  
  
int main() {  
   H^ h = gcnew H;  
   pin_ptr<int> k = &h->j;  
}  
```  
  
 See [Value Type Semantics](../vs140/Value-Type-Semantics.md) for more information.  
  
## __typeof Keyword becomes typeid  
 Managed Extensions typeof syntax:  
  
```  
Array* myIntArray =   
   Array::CreateInstance( __typeof(Int32), 5 );  
```  
  
 New typeid syntax:  
  
```  
Array^ myIntArray =   
   Array::CreateInstance( Int32::typeid, 5 );  
```  
  
 See [typeof Goes to T::typeid](../vs140/typeof-Goes-to-T--typeid.md) for more information.  
  
## See Also  
 [C++/CLI Migration Primer](../vs140/C---CLI-Migration-Primer.md)   
 [(NOTINBUILD)Managed Extensions for C++ Syntax Upgrade Checklist](assetId:///edbded88-7ef3-4757-bd9d-b8f48ac2aada)   
 [New C++ Language Features](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)