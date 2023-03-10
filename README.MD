### Access intrinsic operators through a lookup dict

#### More information: https://docs.python.org/3/library/operator.html

```python
from operatorlookup import doops
print('-------------------------')
print(doops("==", 10, 20))
print(doops("+", 10, 20))
print(doops("-", 10, 20))
print('-------------------------')
defli = list(range(10))
print(defli)
_ = [(doops("=", defli, x, x * 10)) for x in range(10)]
print(defli)
print('-------------------------')
defli = list(range(10))
print(defli)
_ = [(doops("del", defli, 0)) for x in range(10) if x > 5]
print(defli)
print('-------------------------')
defli = {}
print(defli)
_ = [(doops("=", defli, x,x*100)) for x in range(10) if x > 5]
print(defli)
print('-------------------------')
getitemsresult = [(doops("[]", defli, x)) for x in range(10) if x > 5]
print(getitemsresult)


False
30
-10
-------------------------
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[0, 10, 20, 30, 40, 50, 60, 70, 80, 90]
-------------------------
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
[4, 5, 6, 7, 8, 9]
-------------------------
{}
{6: 600, 7: 700, 8: 800, 9: 900}
-------------------------
[600, 700, 800, 900]

# All operations:
from operatorlookup import opdict
print(opdict)
{'+': <function _operator.add(a, b, /)>,
 'concat': <function _operator.concat(a, b, /)>,
 'in': <function _operator.contains(a, b, /)>,
 '/': <function _operator.truediv(a, b, /)>,
 '//': <function _operator.floordiv(a, b, /)>,
 '&': <function _operator.and_(a, b, /)>,
 '^': <function _operator.xor(a, b, /)>,
 '~': <function _operator.invert(a, /)>,
 '|': <function _operator.or_(a, b, /)>,
 '**': <function _operator.pow(a, b, /)>,
 'is': <function _operator.is_(a, b, /)>,
 'is not': <function _operator.is_not(a, b, /)>,
 '=': <function _operator.setitem(a, b, c, /)>,
 'del': <function _operator.delitem(a, b, /)>,
 '[]': <function _operator.getitem(a, b, /)>,
 '<<': <function _operator.lshift(a, b, /)>,
 '%': <function _operator.mod(a, b, /)>,
 '*': <function _operator.mul(a, b, /)>,
 '@': <function _operator.matmul(a, b, /)>,
 'neg': <function _operator.neg(a, /)>,
 'not': <function _operator.not_(a, /)>,
 'pos': <function _operator.pos(a, /)>,
 '>>': <function _operator.rshift(a, b, /)>,
 '-': <function _operator.sub(a, b, /)>,
 'truth': <function _operator.truth(a, /)>,
 '<': <function _operator.lt(a, b, /)>,
 '<=': <function _operator.le(a, b, /)>,
 '==': <function _operator.eq(a, b, /)>,
 '!=': <function _operator.ne(a, b, /)>,
 '>=': <function _operator.ge(a, b, /)>,
 '>': <function _operator.gt(a, b, /)>,
 '+=': <function _operator.iadd(a, b, /)>,
 '&=': <function _operator.iand(a, b, /)>,
 'iconcat': <function _operator.iconcat(a, b, /)>,
 '//=': <function _operator.ifloordiv(a, b, /)>,
 '<<=': <function _operator.ilshift(a, b, /)>,
 '%=': <function _operator.imod(a, b, /)>,
 '*=': <function _operator.imul(a, b, /)>,
 '@=': <function _operator.imatmul(a, b, /)>,
 '|=': <function _operator.ior(a, b, /)>,
 '**=': <function _operator.ipow(a, b, /)>,
 '>>=': <function _operator.irshift(a, b, /)>,
 '-=': <function _operator.isub(a, b, /)>,
 '/=': <function _operator.itruediv(a, b, /)>,
 '^=': <function _operator.ixor(a, b, /)>}
```