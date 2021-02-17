# CPP Errors

This repository keeps track of some common errors occurred in CPP during compilation.

## Content
- [Multiple definition/first defined here](#multiple-definition-first-defined-here-errors)

## “Multiple definition”, “first defined here” Errors

Multiple definition or first defined here errors occurs for several reasons.
- Only include header file without the source file
- Defining function in header file and no source file
- Declaration of function in header file but no definition found in source file for functions.

[link_stackoverflow](https://stackoverflow.com/questions/30821356/multiple-definition-first-defined-here-errors)

## "Symbol lookup error" template

The symbol lookup error can be caused by many issue, here we are going to discuss the cause by template function. If you do not know already, if you want to use a template function you will need to define the template function inside of a header file `hpp` instead of a source file `cpp`.

Example error:
```bash
libanyLibrary.so: undefined symbol: _ZN5utils12param_loader22getGlobalROSParamValueINSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEEPKcEEbRKN3ros10NodeHandleES7_RT_T0_
```
[link_Ubuntu_forum](https://ubuntuforums.org/showthread.php?t=896130)  
[link_gazebo](https://answers.gazebosim.org//question/21417/undefined-symbol-with-plugin/)  
[link_isocpp](https://isocpp.org/wiki/faq/templates#separate-template-class-defn-from-decl)
