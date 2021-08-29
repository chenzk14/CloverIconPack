### ☘ 三叶草图标包模板

[app下载](https://www.coolapk.com/apk/278358)

本图标包模板基于Lollipop的 [SmartIconPack](https://github.com/Mr-XiaoLiang/SmartIconPack) IconCore。有关如何使用IconCore请访问 [SmartIconPack](https://github.com/Mr-XiaoLiang/SmartIconPack) 。

### 💡 准备：

您需要在设备上安装 [Android Studio](https://developer.android.com/studio)

下载本项目，您可以点击本页的绿色“↓Code”按钮，Download Zip，并解压到一个路径不含中文的目录

### ✒ 图标包模板内容修改：

1. 使用 [Android Studio](https://developer.android.com/studio) 打开解压到本地的项目，如何在AS 左侧目录展示结构切换到`Project`选项。

2. 认识主要目录

- [/app/src/main/res](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/res) 主要资源文件存储位置。

- [/app/src/main/asset](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/assets) 图标适配配置文件存储位置2。

- [/app/src/main/res/xml](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/res/xml) 图标适配配置文件存储位置1 + 更新内容配置文件 + 外链列表配置文件。

- [/app/src/main/res/drawable-nodpi](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/res/drawable-nodpi) 图标文件（PNG）存储位置 + 启动页底部图标位置。

- [/app/src/main/res/drawable](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/res/drawable) 其他图片存储位置。

- [/app/src/main/res/values](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/values/) 文字信息，颜色信息，主题信息存储位置。

3. 认识主要文件

- [/app/src/main/res/values-zh/strings.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/values-zh/strings.xml)  文字信息配置文件（中文）

- [/app/src/main/res/values/strings.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/values/strings.xml)  文字信息配置文件（设备默认语言）

- [/app/src/main/res/xml/appfilter.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/xml/appfilter.xml) app适配主要配置文件 [/assets/appfilter.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/assets/appfilter.xml) 内容一样

- [/app/src/main/res/xml/drawable.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/xml/drawable.xml) app适配图标展示主要配置文件 [/assets/drawable.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/assets/drawable.xml) 内容一样

- [/app/src/main/res/xml/links.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/xml/links.xml) 首页外链主要配置文件

- [/app/src/main/res/xml/update.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/xml/update.xml) 历史更新信息主要配置文件

- [/app/src/main/res/drawable/preview_window.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/drawable/preview_window.xml) 启动app时的展示图片配置文件

4. xml文件科普

xml文件一般长这样

```xml

<标签 属性1="属性内容"/>
<标签>真正的内容</标签>
```

也有长这样的

```xml
<外标签>
    <子标签>真正的内容</子标签>
    <子标签>真正的内容</子标签>
</外标签>
```

甚至还有长这样的

```xml
<外标签 属性1="我才是属性内容" 属性2="我才是属性内容">
    <子标签 属性1="我才是属性内容" 属性2="我才是属性内容">真正的内容</子标签>
    <子标签 属性1="我才是属性内容" 属性2="我才是属性内容">真正的内容</子标签>
</外标签>
```

所谓的`标签`其实就是一段描述，描述`真正的内容` 或者 `属性内容`的。所以我们修改其实是修改`真正的内容` 或 `属性内容`，或者增加删除一整个`标签`。标签的`属性`就是用来给标签增加额外的信息。所以如果`真正的内容`想要关联有关属性，那我们就可以这样写：

```xml
<外标签 >
    <子标签 属性1="我现在是真正的内容" 属性2="我现在是真正的内容"/>
    <子标签 属性1="我现在是真正的内容" 属性2="我现在是真正的内容"/>
</外标签>
```

---

#### 🌱 修改图标适配信息 (适合第一次做图标包的朋友看)

当你完成修改后你可以再次点击AS右上方的 绿色三角形按钮，将运行项目到自己手机上查看效果。

如果你需要修改界面上的图片信息，请到app/main/res/drawable下找到您需要更改的图片，名称只能为 小写、下划线、数字的任意组合(不能以数字开头)。如果请确保图片名称是唯一的，尽管后缀名不同也同样需要覆盖掉，将不需要的同名图片删除。

##### 🥑 添加需要适配的图标

图标包适配应用的`关键文件`就在于 [/app/src/main/res/xml](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/res/xml) 下的`appfilter.xml` 和 `drawable.xml`。

它们需要填写的内容大致是这样的：

`appfilter.xml`
```xml
<item component="ComponentInfo{com.android.chrome/com.google.android.apps.chrome.Main}" drawable="ic_chrome"/>
```

`drawable.xml`
```xml
    <category title="系统"/>
    <item drawable="ic_settings" name="设置" />
```

##### 🥑 appfilter.xml

其实很简单，它们两个的内容基本都是这些，首先来看看appfilter.xml

\<item componet="" drawable=""/>这个是不变的格式

其中第一个""中填写的格式为 `需要适配软件的包名` + `/` + `需要适配软件的启动Activity名`，第二个""中填写你的`图标文件名`。

首先， `需要适配软件的包名` + `/` + `需要适配软件的启动Activity名`这个其实不需要你来弄清楚每个软件的这个信息到底是什么样的，因为每个软件都不一样，而且也没法直接看到，所以接下来打开模板app，到第三个页面，也就是适配页面随便选中一个未适配的app，点击下面的发送按钮，发送到你的电脑上，解压后里面有个txt文件，里面已经就已经有你刚才选中的app所需要的信息了。实际上这个txt文件里面就是完整的一行。里面那个drawable="软件名"需要自行修改。

再来看`图标文件名`，这个需要你的图标文件，通常是xxx.png，命名规则是小写字母开头，只允许小写字母和下划线和数字的任意组合。比如ic_chrome.png，现在将你制作的图标文件复制到[/app/src/main/res/drawable-nodpi](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/res/drawable-nodpi)目录里，然后drawable="软件名"替换为drawable="图标文件名"，注意不需要后缀名。

##### 🥑 drawable.xml

这个文件是必须有的，尽管可能没有它也能使用，不过这个文件的主要目的是为了某些桌面可以自由替换某个app的图标，这个时候就会读取drawable.xml里的配置了。它的固定格式为：

```xml
    <category title="类别"/>
    <item drawable="图标文件名" name="APP名" />
    <item drawable="图标文件名" name="APP名" />
    <item drawable="图标文件名" name="APP名" />
    ...
```

首先是一个`<categor title="类别"/>`，这是为了给图标分类，标题随意取，比如`系统`、`游戏`...这个标签写完后就可以在它的下方开始写`<item drawable="图标文件名" name="APP名" />`，`图标文件名`和appfilter一样的做法，`APP名`是对应APP的中文名，其实是可以不写的，但是如果你想写，它可以在模板app内部点击图标后展示name的值，否则默认展示图标文件名。如果不想写可以直接删掉`name="APP名"`，就像这样：

```xml
    <category title="类别"/>
    <item drawable="图标文件名" />
    <item drawable="图标文件名" />
    <item drawable="图标文件名" />
```

以后每一个适配一个新app都需要这样做，当你一个做好一个版本后，别忘了复制appfilter.xml和drawable.xml文件到[/app/src/main/asset](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/assets) 目录下，因为某些桌面使用的是这个目录，不是xml这个目录。

---

#### 🌱 修改图标包内文字信息

###### 🥑 历史更新记录日志

打开 [/app/src/main/res/xml/update.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/xml/update.xml) 历史更新信息主要配置文件。

默认内容：

```xml

    <!--  版本  -->
<version name="1.0" code="5">
    <!--  更新内容，数量不限   -->
    <item>三叶草图标包示例应用</item>
    <item>基于L图标包模板核心组件开发</item>
    <item>开发者QQ：2530767709</item>
</version>

<version name="0.2" code="3">
    <item>增加文本内容配置</item>
    <item>增加图标解析文件的配置</item>
    <item>开发者QQ：1982568737</item>
</version>
...
```

如果这是你的第一个版本，可以将没有用的<version/>标签删除，只保留一个<version/>，然后跟着下方的示例修改

```xml
<version name="你的版本名称比如1.0" code="你的版本序号比如5">
    <!--  更新内容，item数量不限   -->
    <item>更新内容1</item>
    <item>更新内容2</item>
</version>
```

###### 🥑 首页底部链接信息

打开[/app/src/main/res/xml/links.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/xml/links.xml) 首页外链主要配置文件。

默认内容：

```xml
    <!-- 更多应用 -->
    <link
        title="And图标包模板"
        summary="这是另一个完全不一样图标包模板示例应用。"
        icon="and_iconpack"
        url="app_store"
        attr1="org.andcreator.iconpack"/>


    <!-- 友情链接 -->
    <link
        title="为图标包评分吧"
        summary="如果喜欢这个图标包,请给个 ★★★★★"
        icon="ic_launcher_round"
        url="store"/>
        
    <link
        title="开发者的个人网站"
        summary="q(≧▽≦q)q(≧▽≦q)"
        icon="author_icon"
        url="https://bubbble.org"/>
```

这个是差不多的，如果你想在 更多应用下展示外链，请按照上面的那样写，修改xml属性的内容，就像这样，另外不需要有的就直接删除。

```xml
    <!-- 更多应用 -->
    <link
        title="你的应用名称"
        summary="你的应用介绍"
        icon="你的应用图标文件名"
        url="app_store"
        attr1="你的应用包名"/>
```

这时候注意到有一个不一样的东西，那就是你的应用图标，这个图标文件放在哪儿？这个图标文件需要放在- [/app/src/main/res/drawable](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/res/drawable) 其他图片存储位置。命名需要注意最好是小写字母开头，不允许有空格，不允许大写字母，只允许下划线符号。然后填写文件名就好了。


###### 🥑 作者头像名称信息

更改头像请替换[/app/src/main/res/drawable/author_icon.png](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/drawable/author_icon.png)。

作者名称和介绍需要修改以下两个位置：

- [/app/src/main/res/values-zh/strings.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/values-zh/strings.xml)  文字信息配置文件（中文）

- [/app/src/main/res/values/strings.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/values/strings.xml)  文字信息配置文件（设备默认语言）

```xml
    <string name="maker_name">Andrew Martin</string>
    <string name="maker_sign">你好😉！我一名设计摄影爱好者，也是本图标包UI界面的创作者，希望有更多人喜欢这个作品！</string>
```

相信这么聪明的你一下子就知道该怎么修改了吧。

---

#### 🌱 修改图标包其他信息

###### 🥑 APP名称

查看以下两个文件

- [/app/src/main/res/values-zh/strings.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/values-zh/strings.xml)  文字信息配置文件（中文）

- [/app/src/main/res/values/strings.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/values/strings.xml)  文字信息配置文件（设备默认语言）

```xml
<resources>
    <string name="app_name">你的图标包模板</string>
</resources>
```

###### 🥑 APP包名

打开 [/app/build.gradle](https://github.com/hujincan/CloverIconPack/blob/master/app/build.gradle) 找到这一行

```groovy
    applicationId "org.bubbble.clovericonpack"
```

直接将`org.bubbble.clovericonpack` 修改为你的包名，命名规范是一个能代表你自己的域名倒着写，然后+你的图标包名称，全部小写。

###### 🥑 APP版本号

打开 [/app/build.gradle](https://github.com/hujincan/CloverIconPack/blob/master/app/build.gradle) 找到这一行

```groovy
    versionCode 1
    versionName "1.0"
```

versionCode 每次更新都要比前一次大
versionName "" 命名随意，一般都是1.0，1.1之类的。

###### 🥑 APP图标

找到AS左侧的目录，鼠标右击一个res下的目录，选择 new -> Image assst，然后会弹出一个桌面图标编辑器，具体使用可以Google搜索一下。

###### 🥑 APP启动页图标

打开 [/app/src/main/res/drawable/preview_window.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/drawable/preview_window.xml)  以及 [/app/src/main/res/drawable-anydpi-v23/preview_window.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/drawable/preview_window.xml) 启动app时的展示图片配置文件。

将其修改为

```xml
<?xml version="1.0" encoding="utf-8"?>
<layer-list xmlns:android="http://schemas.android.com/apk/res/android">

    <item android:drawable="@color/activity_background" />

    <item>
        <bitmap
            android:gravity="center"
            android:src="@drawable/start_window_logo" >
        </bitmap>
    </item>
</layer-list>
```

然后你可以将一个自己制作额启动图标放到 [/app/src/main/res/drawable-nodpi](https://github.com/hujincan/CloverIconPack/tree/master/app/src/main/res/drawable-nodpi) 其他图片存储位置。将其命名为`start_window_logo`，后缀名可以是png或者jpg

###### 🥑 APP主题颜色

打开 [/app/src/main/res/values/colors.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/values/colors.xml) 找到

```xml
    <color name="color_primary">#43a047</color>
```

修改`#43a047`为你自己想要颜色。另外夜间模式的颜色也要改一下，打开 [/app/src/main/res/values-night/colors.xml](https://github.com/hujincan/CloverIconPack/blob/master/app/src/main/res/values-night/colors.xml)  修改暗色下的主题色，颜色饱和度降低。

---

### 😜 软件截图

<img src="https://github.com/hujincan/CloverIconPack/blob/master/screenshot/Screenshot_2.png?raw=true"/>

<img src="https://github.com/hujincan/CloverIconPack/blob/master/screenshot/Screenshot_1.png?raw=true"/>
