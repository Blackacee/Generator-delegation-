# Generator-delegation-

function* g1() {
 yield 2;
 yield 3;
 yield 4;
}
function* g2() {
 yield 1;
 yield* g1();
 yield 5;
}
var it = g2();
console.log(it.next()); // 1
console.log(it.next()); // 2
console.log(it.next()); // 3
console.log(it.next()); // 4
console.log(it.next()); // 5
console.log(it.next()); // undefined
