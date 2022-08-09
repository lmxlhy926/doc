去年干过类似的事，把一个 C++底层的库和一堆依赖 library 、 test 程序移植到了 Android 上。我不是专门搞 Android 的，所以纯粹是站在一个 Linux C++ developer 上的一些经验，不知道对你有没有帮助。

如果是 C\C++的程序，基本流程可能是这样的，先把它编成 Android 上的 native 程序（这一步没有什么 Android 特有的东西在里面，就和移植到任何平台一样），具体来说，找到对应的交叉编译器(NDK)，选择你习惯的 make 工具，编译你的代码。然后就可以尝试通过 ADB 把编完的程序上传到 android 上跑，上传、运行等都可以通过 adb （有大把的教程） 。等以上 native 跑通了，再去搞 APK ，用 JNI 去封装一个 java 层，一种方法是把你的程序编成一个 shared library ，然后在 wrapper 层里去 dlopen 你的 library ， dlsym 其中的 main ，然后执行等等，这一步有很多 tricky 的地方，比如 linux 下的环境变量在 Android 上怎么处理，或者窗口的 handle 怎么传递等等。



**交叉编译**：交叉编译器(NDK)，make工具，编译代码

ADB：将代码上传到android上跑。

APK：用JNI封装一个java层



NDK就是帮助我们可以在Android应用中使用C/C++来完成特定功能的一套工具.

 1.首先NDK可以帮助开发者“快速”开发C(或C++)的动态库。
 2.其次，NDK集成了“交叉编译器”。使用NDK，我们可以将要求高性能的应用逻辑使用C开发，从而提高应用程序的执行效率。

































