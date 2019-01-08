Goal:
no-hoisting of submodule dependencies.

Therefore a should not contain the @types of b, c and d in a/node_modules/@types.

Package dependencies:
a -> b

b -> c
b -> d

c -> d

