# Kotlin Koans

# Pengenalan Kotlin (Lambdas, Extension Functions, Smart Casting dll)

![](https://cdn-images-1.medium.com/max/2000/0*vQbXdL560uApNu54)
<span class="figcaption_hack">Photo by [Ben
Kolde](https://unsplash.com/@benkolde?utm_source=medium&utm_medium=referral) on
[Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)</span>

Kotlin merupakan Bahasa Pemrograman *modern* yang bersifat **statically-typed**
yang dapat di jalankan di atas **platform Java Virtual Machine(JVM) **. Google
juga sudah meresmikan bahwa kotlin merupakan official language untuk
mengembangkan aplikasi android karena ekspresif, ringkas, dan powerfull. dan
juga dapat dijalankan berdampingan dengan bahasa Java

Pada artikel ini akan membahas latihan kotlin dari website resmi kotlin .
website ini sangat bagus untuk memahami kotlin karena disediakan challenge dan
task-task yang membantu memahami kotlin itu sendiri

### **1. Hello World**

Membuat method di kotlin menggunakan fun

    fun main(args: Array<String>) {
        println("Hello, world!")
    }

More Detail
:[http://kotlinlang.org/docs/reference/basic-syntax.html#defining-functions](http://kotlinlang.org/docs/reference/basic-syntax.html#defining-functions)

### **2. Switch Case di Kotlin**

    var score = 9
    var grade = when (score) {
    	9, 10 -> "Excellent"
    	in 6..8 -> "Good"
    	4, 5 -> "OK"
    	in 1..3 -> "Fail"
    	else -> "Fail"
    }
    print(grade) //Excellent

### **3. Named Arguments**

Named Argument sangat berguna apabila dalam method yang memiliki paramater yang
banyak dan kita hanya ingin merubah beberapa parameter saja,

     

Seperti contoh dibawah ini kita ingin mengganti value dari parameter prefix dan
postfix sehingga sesuai dengan format berikut : [a, b, c]

Berikut ini Codenya untuk merubah prefix dan postfix sehingga sesuai dengan
hasil yang diinginkan

     

More
Detail:[http://kotlinlang.org/docs/reference/functions.html#default-arguments](http://kotlinlang.org/docs/reference/functions.html#default-arguments)

### **4. Default Arguments**

Default Argument berguna untuk set default value sehingga kita tidak perlu
membuat beberapa constructor dan tentunya dapat meminimalkan baris kode kita ,
Berikut ini adalah Contoh overloads in Java


Code tersebut dapat kita ringkas menggunakan Kotlin dengan menset Default
Argument untuk value number dan boolean toUppercase


Jadi kodingan diatas itu menset nilai default 42 dan untuk toUpperCase = False

jadi ketika toUpperCase tidak diganti true maka namanya tidak diganti menjadi
UpperCase jadi dia hanya akan balikin nama dengan huruf kecil dan number

More Detail:
[http://kotlinlang.org/docs/reference/functions.html#default-arguments](http://kotlinlang.org/docs/reference/functions.html#default-arguments)

### **5. Lambdas**

Kotlin juga support untuk functional Programming, Jadi disini mendapatkan semua
argumen angka kemudian datanya di passing ke **it** dan di cek apakah genap atau
tidak

jika ada angka yang genap maka akan mengembalikan nilai true dan jika tidak
terdapat angka genap maka akan mengembalikan nilai false

     

it itu mereferensikan sebagai collection jadi sama saja seperti ini

*collection %2 ==0*

More Detail:
[http://kotlinlang.org/docs/reference/lambdas.html](http://kotlinlang.org/docs/reference/lambdas.html)

### **6. Data classes**

Ini salah satu yang powerfull di kotlin dibandingkan java yaitu kita tidak perlu
membuat setter dan getter seperti java di bawah ini

> Java


Dibanding Code diatas yang memakan beberapa line code , di kotlin bisa kita
sederhanakan menjadi :

> Kotlin


More Detail :
[https://kotlinlang.org/docs/reference/data-classes.html](https://kotlinlang.org/docs/reference/data-classes.html)

### **7. Nullable types**

value null merupakan hal yang patut diwaspadai karena akan meyebabkan error maka
dari perlu mengecek terlebih dahulu apakah valuenya null atau tidak

Tentu untuk mengecek tersebut membuat kodingan kita semakin banyak dan kurang
rapi

> Java

     

Hal Tersebut dapat disederhanakan di Kotlin yaitu menggunakan ‘**?’ **berguna
untuk mengecek apakah valuenya null atau tidak sehingga bisa meringkas kode dan
lebih rapi

> Kotlin

     

### **8. Smart Casting**

di Java kita perlu memberikan Casting sesuai dengan object seperti contoh
dibawah ini kita perlu casting Car

> Java

    if (object instanceof Car) {
       Car car = (Car) object;
    }

> Kotlin

di Kotlin kita tidak perlu melakukan casting tinggal disimpan saja ke variable
car

    // if object is null
    if (object is Car?) {
       var car = object // smart casting, car will be null
    }

### **9. Extension Function**

Extension Function sangat berguna untuk meringkas kode karena kita hanya perlu
memanggil dengan menggunakan **“.” **karena kita membuat function nya dengan
format **fun String.removeFirstLastChar()**


Link
Referensi:[https://www.programiz.com/kotlin-programming/extension-functions](https://www.programiz.com/kotlin-programming/extension-functions)

### **10. Objects Expression**

Gunanya Object Expression adalah ketika kita ingin merubah beberapa dalam sebuah
class atau interface tanpa mendeklarasikan subclass


Contoh diatas kita memodifikasi method eat() dari Person sehingga hasil
Outputnya seperti ini

    Eating Vegetable.
    Talking with people.
    Praying god.

### **11. SAM conversions**

Override Class yang hanya memiliki satu method dari kelas Java , SAM berguna
karena API Android kebanyakan masih pakai Java tapi misalkan Third Party atau
class yang dipakai memakai Kotlin maka kita tidak perlu menggunakan SAM
Conversions

     
     

     

     
     



     
     
     
     

     


Kita memanggilnya



[Klik More
Detail](https://code.tutsplus.com/tutorials/quick-tip-write-cleaner-code-with-kotlin-sam-conversions--cms-29304)

### **12. Extension functions on collections**

Disini Kita akan Menggunakan Functions sortedDescending()

    fun getList(): List<Int> {
        return arrayListOf(1, 5, 2).sortedDescending()
    }

Jadi kita memanggilnya hanya menggunakan **‘titik’** untuk memanggil fungsi
sortedDescending untuk mengurutkan angkanya

Link Referensi :

* [Kotlin](https://medium.com/tag/kotlin?source=post)
* [Programming](https://medium.com/tag/programming?source=post)
* [Android App
Development](https://medium.com/tag/android-app-development?source=post)
* [Kotlin Beginners](https://medium.com/tag/kotlin-beginners?source=post)

# Conventions di Kotlin (Comparison,For Loop,Destructure Declaration dll)

<span class="figcaption_hack">“A man reading his book while sitting on a bench in a meadow” by [Ben
White](https://unsplash.com/@benwhitephotography?utm_source=medium&utm_medium=referral)
on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)</span>

### 1. Comparison

Berguna untuk membandingkan antar value, Seperti Contoh dibawah ini kita
membandingkan Apple dengan Banana dan hasilnya Apple lebih kecil karena sesuai
abjad lebih dulu ‘A’ daripada ‘B’

        var a = "Apple"
     
        var b = "Banana"
        var result = a.compareTo(b)
        if(result==0){
            println("Strings '$a' and '$b' are equal.")
        } else if(result < 0){
            println("'$a' is less than '$b' lexically.") // Print this
        } else{
            println("'$a' is Greater than '$b' lexically.")
        }

### 2. In Range

Mengecek apakah terdapat dalam list, seperti contoh dibawah ini

yang pertama akan return true karena terdapat a didalam list

yang kedua akan return false karena terdapat a didalam list


### 3. For Loop

For Loop merupakan salah satu penerapan In range yang digunakan berulang-ulang
atau digunakan di for. Bentuknya sendiri lebih mirip seperti For-each jika dalam
bahasa lainnya.

Seperti contoh dibawah ini akan berulang-ulang dalam range 1–5

dan Contoh yang kedua akan berulang dalam range {6–0 dan lompat 2 sehingga
menghasilkan 6420

    for (i in 1..5) {
        println(i) // 12345
    }

    //6 tidak termasuk hitungan dan lompat 2
    for (i in 6 downTo 0 step 2) {
        print(i) //6420
    }

### 4. Operators Overloading

Kotlin memiliki beberapa operator seperti + atau * , dan kita bisa
menggunakannya dengan mudah pada kelas. Seperti contoh dibawah ini kita
menggunakan operator plus untuk MyDate dengan timeInterval


### 5. Destructure Declaration

Berguna untuk memudahkan kita dalam menginisiasi value from object, seperti
contoh dibawah ini kita menginisiasi year,month dan dayOfMonth dari date


    fun isLeapDay(date: MyDate): Boolean {

    val (year, month, dayOfMonth) = date // simple declaration

    // 29 February of a leap year
        return year % 4 == 0 && month == 2 && dayOfMonth == 29
    }

Sebenarnya proses dibaliknya Seperti Dibawah ini


    fun isLeapDay(date: MyDate): Boolean {

    val year = date.component1() 
    val month = date.component2()
    val dayOfMonth= date.component3()

    // 29 February of a leap year
        return year % 4 == 0 && month == 2 && dayOfMonth == 29
    }

* [Programming](https://medium.com/tag/programming?source=post)
* [Kotlin](https://medium.com/tag/kotlin?source=post)
# Collections di Kotlin (Filter,Map,Sort ,dll)

![](https://cdn-images-1.medium.com/max/2000/0*m_i7du7-gbbz515O)
<span class="figcaption_hack">Photo by [Rana
Sawalha](https://unsplash.com/@ranasawalha?utm_source=medium&utm_medium=referral)
on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)</span>

### 1. Filter, Map

Filter berguna untuk mendapatkan value yang sesuai dengan kondisi yang
ditentukan

     

Seperti Contoh diatas hasilnya adalah 1 dan 2 karena -1 itu kurang dari 0
sehingga tidak sesuai dengan kondisi yang ditentukan

Map Berguna untuk menghitung semua value yang terdapat dalam variabel

     

Sesuai contoh diatas dengan menggunakan map maka akan menghitung semua angka
yang terdapat di numbers dikali dengan 2 sehingga menghasilkan 2,-2 dan 4

### 2. All , Any and other predicate

All berguna untuk mengecek apakah semua valuenya sesuai dengan kondisi yang
ditentukan


Sehingga akan menghasilkan false karena tidak semua value adalah nol

Any berguna untuk mengecek apakah terdapat value yang sesuai dengan kondisi yang
ditentukan


Sehingga akan menghasilkan true karena terdapat minimal 1 value yang sesuai

Count berguna untuk menghitung jumlah value yang sesuai dengan kondisi

     

Sehingga akan menghasilkan 1 karena hanya terdapat satu value yang sesuai dengan
kondisi

find berguna untuk mencari value yang sesuai dengan kondisi


Sehingga akan menghasilkan 2 karena hanya 2 yang lebih dari nol

### 3. FlatMap

flatmap berguna untuk mengupdate list menjadi 1 karakter


### 4. Max,Min

fungsi ini berguna untuk menentukan value minimum atau maximum yang terdapat di
list

yang pertama berguna untuk menentukan angka yang paling besar

dan yang kedua menentukan kata yang memiliki panjang yang paling sedikit


### 5. Sort

berguna untuk mengurutkan value yang terdapat di list

yang pertama mengurutkan value berdasarkan urutan

dan yang kedua mengurutkan value berdasarkan panjang kata

     

### 6. Sum

Berguna untuk menjumlahkan value yang terdapat di list seperti contoh dibawah
ini

yang pertama menjumlahkan angka yang terdapat di list

dan yang kedua menjumlahkan panjang dari panjang kata di list

     

### 7. GroupBy

berguna untuk mengelompokkan value yang sama seperti contoh dibawah ini
mengelompokkan berdasarkan panjang karakter

     

### 8. Partition

berguna untuk memisahkan value yang sesuai dan yang tidak sesuai dengan kondisi,
seperti contoh dibawah ini berguna untuk memisahkan value yang negative dan
positive

     

### 9. Fold

Berguna untuk mengolah data antara value sebelumnya dengan setelahnya

     

Jadi contoh diatas kita akan mengalikan antar bilangan

Jadi pertama partProduct = 4 dan elementnya = 1 -> 4

partProduct = 4 dan elementnya = 2 -> 8

partProduct = 8 dan elementnya = 3 -> 24

partProduct = 24 dan elementnya = 4 -> 96

* [Kotlin](https://medium.com/tag/kotlin?source=post)

# Penggunaan Lateinit , Lazy Property dan Custom Delegates Class

<span class="figcaption_hack">“A focused man working on a sticker-covered laptop in a coffee shop” by [Tim
Gouw](https://unsplash.com/@punttim?utm_source=medium&utm_medium=referral) on
[Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)</span>

### 1. Lateinit

Lateinit digunakan ketika kita ingin membuat non-null type tapi kita
menginisiasikannya melalui dependency injection atau disebuah method setup dalam
unit test

Seperti contoh dibawah ini , kita menginginkan property subject non-null type
tapi kita menginisiasi valuenya di method setup

Sedangkan jika kita menggunakan non-null type yang biasanya kita perlu
menginisiasikan value null terlebih dahulu

     
     MyTest {     
        
     
     subject: TestSubject      

        @SetUp 
     setup() {         
           subject = TestSubject()     
        }      
        
        @Test 
     test() {         
            subject.method()  // dereference directly      
        } 
    }

### 2. Lazy Property

Jika kita menggunakan lateinit atau nullable type , variabelnya dapat diganti
karena menggunakan var dan sedangkan kita ingin membuat variabel yang tidak
dapat diganti dan non-null type

Maka dari itu terdapat Lazy property yang berguna untuk membuat tipe non-null
tapi read-only jadi tidak bisa dirubah lagi

Seperti Contoh dibawah kita mau membuat read-only property tetapi karena kita
menggunakan val jadi kita tidak bisa menginisiasi lagi

    class MainActivity : AppCompatActivity() {
        private 
     mWelcomeTextView: 

    override fun onCreate(savedInstanceState: Bundle?) {
            super.onCreate(savedInstanceState)
            setContentView(R.layout.
    )

        }
    }

Jadi solusinya menggunakan Lazy Property dengan menginisiasi variabel ketika
dipanggil sehingga kita bisa membuat properti yang not-null dan read-only
sehingga tidak bisa dirubah lagi.

    class MainActivity : AppCompatActivity() {
        private val messageView : TextView 
    // runs on first access of messageView
            
        

    override fun onCreate(savedInstanceState: Bundle?) {
            super.onCreate(savedInstanceState)
        }

    fun onSayHello() {
            // Initialization would be run at here!!
            
    .
    = "Hello"
        }
    }

### 2. Delegates Class

Delegates Class harus mengimplementasikan interface`ReadOnlyProperty` and
`ReadWriteProperty `dan harus terdapat `operator`methods

Kita bisa mendelegasikan property dengan cara `by <delegate>` format :

    val / var <property name>: <Type> 
     <delegate>

Kita bisa membuat class delegates property seperti dibawah ini

    class Delegate {
        
    (
                thisRef: Any?,
                property: KProperty<*>
        ): String {
            print("Delegate Value")
        }

    (
                thisRef: Any?,
                property: KProperty<*>, value: String
        ) {
            print("New Assign Value")
        }
    }

    var e : String by Delegate()

    print(e) //Print “Delegate Value”

    e=”Value” //Print “New Assign Value”

jadi ketika kita memanggil value maka kita memanggil method getValue

dan jika kita menset value maka kita memanggil method setValue

Link referensi:

* [Android](https://medium.com/tag/android?source=post)
* [Kotlin](https://medium.com/tag/kotlin?source=post)

# Perbedaan Standart Function With , Run , Let , Also dan Apply di Kotlin

<span class="figcaption_hack">Photo by
[rawpixel](https://unsplash.com/@rawpixel?utm_source=medium&utm_medium=referral)
on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)</span>

Mungkin beberapa orang ada yang masih bingung dengan perbedaan standart function
yang terdapat di kotlin dan bingung untuk menentukan yang mana yang tepat untuk
digunakan.

Disini saya akan menjelaskan perbedaan penggunaan antara standart function dan
cara menentukan function yang tepat untuk digunakan.

### Scoping functions

Artikel ini akan berfokus pada run, with, T.run,T.let and T.apply. ini adalah
scope functions, seperti contoh dibawah ini

    fun test() {
        var mood = "I am sad"
        
    {
            val mood = "I am happy"
            
    (mood) // I am happy
        }
        
    (mood)  // I am sad
    }

Jadi gunanya scope function yaitu membuat lingkup sendiri sehingga tidak merubah
value yang berada diluarnya

### 3 attributes of scoping functions

#### 1. Normal vs. extension function

Jika kita lihat `with` dan`T.run`, keduanya memiliki kegunaan yang hampir sama.
berikut ini adalah kesamaan keduanya

    (webview.
    ) {
        
    = true
        
    = true
    }

    // similarly

    webview.settings.
     {
    = true
        
    = true
    }

Tetapi `with`, merupakan normal function sedangkan `T.run` adalah extension
function .

Lalu apa perbedaannya ? kenapa tidak pakai with saja?

bayangkan jika kita perlu mengecek null , jika kita menggunakan with maka kita
perlu menambahkan disemua variabelnya. jadi lebih simple menggunakan T.run untuk
mengecek nullability sebelum menggunakannya

    // Yack!
    (webview.
    ) {
    = true
          
    = true
       }
    }

    // Nice.
    webview.settings?.
     {
    = true
        
    = true
    }

#### 2. This vs. it argument

Jika kita melihat`T.run` dan`T.let`, keduanya juga memiliki fungsi yang hampir
sama

    stringVariable?.
     {
          println("The length of this String is $length")
    }

    // Similarly.

    stringVariable?.
     {
          println("The length of this String is ${
    .length}")
    }

Perbedaanya adalah kalo T.run mereferensikan T sebagai this jadi seperti contoh
diatas itu merepresentasikan ${this.length} atau ${stringsVariable.length}. jadi
**this sebagai argumen**

Sedangkan T.let mengirimkan dirinya sendiri kedalam fungsi, jadi ini merupakan
lambda argumen sehingga it merupakan T itu sendiri. seperti contoh diatas
${it.length} itu sama saja dengan ${stringVariable.length}

Kita juga bisa mengganti nama argumen seperti dibawah ini

    stringVariable?.
     {
          
     ->
          println("The non null string is 
    ")
    }

#### 3. Return this vs. other type

Terdapat perbedaan antara let da also

Ketika kita menggunakan let maka kita melemparkan value ke proses selanjutnya
Seperti contoh dibawah ini ketika let sebelumnya menulis it.reversed maka di let
setelahnya akan mengacu ke value yang telah di reverse

Berbeda dengan also karena also akan melemparkan value aslinya sehingga tidak
memiliki ketergantungan dengan also sebelum maupun setelahnya

    val original = "abc"

    // Evolve the value and send to the next chain
    original.
    {
        
    ("The original String is $
    ") // "abc"
        it.
    () // evolve it as parameter to send to next let
    }.
    {
        
    ("The reverse String is $
    ") // "cba"
        it.length  // can be evolve to other type
    }.
    {
        
    ("The length of the String is $
    ") // 3
    }

    // Wrong
    // Same value is sent in the chain (printed answer is wrong)
    original.
    {
        
    ("The original String is $
    ") // "abc"
        it.
    () // even if we evolve it, it is useless
    }.
    {
        
    ("The reverse String is ${
    }") // "abc"
        it.length  // even if we evolve it, it is useless
    }.
    {
        
    ("The length of the String is ${
    }") // "abc"
    }

    // Corrected for also (i.e. manipulate as original string
    // Same value is sent in the chain 
    original.
    {
        
    ("The original String is $
    ") // "abc"
    }.
    {
        
    ("The reverse String is ${
    }") // "cba"
    }.
    {
        
    ("The length of the String is ${
    }") // 3
    }

### Looking at all attributes

Apply itu merepresentasikan sebagai this dari objectnya, seperti contoh dibawah
ini kita bisa memanggil action dan data yang merupakan bagian dari Intent()

    // Improved approach, chaining
    fun createIntent(intentData: String, intentAction: String) =
            Intent().
    { 
    = intentAction }
    .
    { 
    = Uri.parse(intentData) }

cara kerjanya sama seperti dibawah ini kita memanggil intent.action dan
intent.data

    // Normal approach
    fun createIntent(intentData: String, intentAction: String): Intent {
        val intent = Intent()
        intent.
    = intentAction
    intent.
    =Uri.parse(intentData)
        return intent
    }

### Function selections

berikut ini panduan untuk menentukan pilihan function apa yang cocok digunakan

Thans to [Elye](https://medium.com/@elye.project) , This is Original Post :

* [Kotlin](https://medium.com/tag/kotlin?source=post)

From a quick cheer to a standing ovation, clap to show how much you enjoyed this
story.

### [Ahmad Taufiq](https://medium.com/@ataufiq665)

Information System Student in Telkom University





