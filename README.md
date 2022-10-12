# Değişken Tanımlama
### 1-Var ES5 de kullanılan değişken atama yöntemidir. Var ile oluşturulan değişkenlere her yerden ulaşabildiği için sorunlar yaratmaktadır.
```
var x=5;
{
var x=10;
}
console.log("X Degeri:"+x)
```
> X Degeri:10
### 2-Let blok kapsamlı olarak değişken tanımamıza olanak tanır.
```
let x=5;
{
let x=10;
}
console.log("X Degeri:"+x)
```
> X Degeri:5
### 3-Const let gibi çalışır fakat değeri sonradan değiştirilemezdir.
```
const x=5;
{
const x=10;
}
console.log("X Degeri:"+x)
```
> X Degeri:5

# Spread (...) Operatörü
### 1- ... operatörü, bir öğeyi daha fazla öğeye genişletir.
```
const arabalar = ["Tofaş", "Volvo", ..."BMW"];
console.log(arabalar)
```
>["Tofaş","Volvo","B","M","W"]

### 2- ... operatörü, iki dizinin öğelerini birleştirir.
```
const arabalar1 = ["Tofaş", "Volvo", "BMW"];
const arabalar2=["Ford","Wolkswagen"]
const tumAraclar=[...arabalar1,...arabalar2]

console.log(tumAraclar)
```
>["Tofaş","Volvo","BMW","Ford","Wolkswagen"] 

### 3- ... operatörü, bir dizideki öğeye çağrı yapıldığında bağımsız bir değişkene atamak için kullanılır.
```
const numbers = [23,55,21,87,56];
let maxValue = Math.max(...numbers);

console.log(maxValue)
```
>87

# Hazır Metodlar
### 1-Includes -> Başvurulan dizi bizim belirttiğimiz değeri içeririyorsa true/değilse false döner.
```
let text = "Merhaba Dünya";
console.log(text.includes("Merhaba"))
```
> true   
### 2-Keys -> Başvurulan dizinin anahtar değerlerini dizi şeklinde döner.
```
const meyveler = ["Elma", "Armut", "Kavun", "Çilek"];
let keys=meyveler.keys();
let text = "";
for (let x of keys) {
  text += x;
}
console.log(text) 
```
> 0123
### 3-Values -> Başvurulan dizinin değerlerini dizi şeklinde döner.
```
const meyveler = ["Elma", "Armut", "Kavun", "Çilek"];
let values=meyveler.values();
let text = "";
for (let x of values) {
  text += x;
}
console.log(text) 
```
> ElmaArmutKavunÇilek
