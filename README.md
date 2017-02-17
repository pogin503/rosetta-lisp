lispboot
========

lispboot is a general boot code used in [ocalisp](https://github.com/yubrot/ocalisp).

## Required syntax

* `(def sym x)` - Evaluates `x`, and then binds `sym` to the result of `x` on the current environment. Produces `()`.
* `(set! sym x)` - Evaluates `x`, and then overwrites a variable named `sym` on the current environment. Produces `()`.
* `(begin ...)` - Evaluates arguments sequentially and produces the result of the last argument.
* `(if cond a b)` - Evaluates `cond`, and then evaluates `a` if the result of `cond` is not `#f`, or otherwise evaluates `b`. Produces the result of `a` or `b`.
* `(fun params ...)` - Produces a function.
* `(macro params ...)` - Produces a macro.
* `(builtin sym)` - Produces a builtin function named `sym`.
* `(quote x)` - Produces `x` as data without evaluating it.

## Required builtin functions

```
(cons a b)
(exit exitcode)
(error msg)
(print strs...)
(println strs...)
(concat strs...)
(show x)
(gensym)
(+ nums...)
(- num nums...)
(* nums...)
(/ num nums...)
(% num nums...)
(= xs...)
(< nums-or-strs...)
(> nums-or-strs...)
(<= nums-or-strs...)
(>= nums-or-strs...)
(apply f args)
(car cons)
(cdr cons)
(num? x)
(sym? x)
(str? x)
(cons? x)
(nil? x)
(bool? x)
(proc? x)
(call/cc fun)
(eval s)
(macroexpand s)
(macroexpand-1 s)
```

