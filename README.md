Download link :https://programming.engineering/product/ga1-2-a-type-checker-for-cmm-overload/


# GA1.2.-A-Type-Checker-for-Cmm-overload
GA1.2. A Type Checker for Cmm – overload
A Type Checker for Cmm Supporting Implicit Type Coercions and Operator Overloading – Overloading

The purpose of this question is to help the student master:

• Understand the concept of using types to resolve overloading of operators as used in C

0 Open workspace

Using VSCode – General Instructions Problem Background

Problem

• Write a function overload_binop : untyped_binop —> numeric_type —> (typed_binop * numeric_type) option that is given an untyped binary operator and a type to which the desired typed binary operator can be applied, possibly after promoting the arguments to a greater type, if the type is a numeric type. The function overload_binop returns the typed version of the binary operator capable of taking arguments of the given type, paired with the required type for its arguments (the type to which they may need to be promoted). If that type is a numeric type, the operator should be chosen to take as arguments ones of the least type greater than or equal to the given type.

• Write a function overload_monop : untyped_monop —> numeric_type —> (typed_monop * numeric_type) option that implements the same behavior for monadic operators.

Note: • • You will be given in Plsolutions the functions from the cmm_promote question: o ► numeric_type_less : numeric_type —> numeric_type —> boot

o Based on the ordering above, vat max_numeric_type : numeric_type —> numeric_type —> numeric_type = <fun>

o ► vat promote_to_numeric_type : (typed_monop, typed_binop) exp * numeric_type —> numeric_type —> (typed_monop, typed_binop) exp option = <fun>

O ► vat promote : (typed_monop, typed_binop) exp * exp_type —> exp_type —> (typed_monop, typed_binop) exp option = <fun> • Similar functionality will be needed for monadic operators when translating untyped expressions built from monadic operators to typed ones. You may choose whether to write a helper function for that in the file for that question, or to inline that functionality.
