# UpSchool-Android-Bootcamp
 
# Araştırma Ödevleri:
 
- [Araştırma Projesi 1 - Lateinit](#1)
- [Araştırma Projesi 2 - Tools Namespace](#2)
- [Araştırma Projesi 3 - Font family XML](#3)
 
 
### <a name="1"></a> Araştırma Projesi 1
 
- Lateinit neden kullanıyoruz?
- Lateinit kullanımından bahseder misiniz?
- Lateinit için bir örnek kullanım gösterir misiniz ?
 
In Kotlin, the lateinit keyword is used for those variables which are initialized after the declaration or we can say that the variable which is late initialized is called a lateinit variable. There are many cases when you need to create a variable but you don't want to initialize it at the time of declaration/creation of the variable because you are sure that the variable will be initialized before its access/usage.
 
One way of achieving this is by making the variable nullable like this:
 
-private var courseId: String? = null
 
If we don't want to make nullable we can use the lateinit keyword. It will not allocate memory until initialized.
 
-private lateinit var myViewModel: MyViewModel
 
 
 
 
### <a name="2"></a> Araştırma Projesi 2
 
 
- Layout dizini içinde xml dosyalarımız için kullandığımız namespace nedir ?
- Neden kullanılmaktadır ?
- Nasıl kullanılmalıdır ?
- Bir adet Tools (tools namespace) attribute kullanımını gösterir misiniz ? 
 
Namespacing does for functions and classes what scope does for variables. It allows you to use the same function or class name in different parts of the same program without causing a name collision.
If we didn't have namespaces we'd have to (potentially) change a lot of code any time we added a library, or come up with tedious prefixes to make our function names unique. With namespaces, we can avoid the headache of naming collisions when mixing third-party code with our own projects.
 
Here I have an example,
 
![code](https://user-images.githubusercontent.com/66526972/163675117-e067a456-232e-4f93-a16a-8532a264b094.png)

### <a name="3"></a> Araştırma Projesi 3
- Font family dosyası nasıl oluşturulup kullanıyoruz? 
- Niçin böyle kullanımı tercih ediyoruz ?

Google Fonts provide a wide variety of fonts that can be used to style the text in Android Studio.There are majorly three methods to add custom fonts to text in Android StudioThe first two methods involve the use of the Typeface class but we’re going to talk about the third method which is quite direct and easy.

With Android 8.0 (API Level 26) a simpler method was introduced for using fonts as a resource in Android Studio. The android:fontFamily attribute of the TextView class is used to specify the font.

- Advantages:

We can create a font family as an XML resource and access it as a single unit, instead of referencing each style and weight as separate resources.

- Disadvantages:

While the method seems easy and time-saving, however, it bundles the extra files with the APK of the app which might increase its size. Though this also ensures that the fonts are present even when the app works offline.

- To create a font family, perform the following steps in the Android Studio:

1- Right-click the font folder and go to New > Font resource file. The New Resource File window appears.

2- Enter the file name, and then click OK. The new font resource XML opens in the editor.

3- Enclose each font file, style, and weight attribute in the <font> element. (developer.android.com)


