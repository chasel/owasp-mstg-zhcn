# 手机应用分类

"手机应用" 指的是设计在手机设备上独立运行的计算机程序。今天，Android和iOS占有手机操作系统90%以上的市场份额。另外，历史上第一次手机网络使用超过桌面系统，网络应用在手机浏览和应用上使用最广泛。

> 在该指南内，我们使用 "应用" 术语作为通用词代指运行在手机操作系统上任何应用程序。

通常意义上，应用被设计为直接运行在系统上，或在智能手机设备的浏览器上，或两者兼有。接下来的每个章节，我们将定义不同场景下手机应用类别的特点并讨论各自的不同点。

## Naitve 应用
手机操作系统，包括Android和iOS，都带有软件开发包(SDK)用于不同系统的应用开发。这样的程序被称为针对对应系统开发的 Native 应用。当我谈论这些应用时，通常意义上来讲，他是使用各自操作系统上的标准程序语言(比如 iOS 上的 Objective-C 或 Swift 和 Android 上的 Java或 kotlin)开发的 Native 应用。

Native 应用固有的特点能提供更快的性能和最高的可靠性。他们通常遵循平台特定的设计原则(比如, [Android设计规范]())，该情况导致相比 Hybrid和web 应用在用户界面上体验更加一致。因为他们跟操作系统结合得更紧密，Native 应用能直接访问设备上绝大多数的组件(比如相机，感应器，硬件密钥库等)。

当我们讨论Android Native 应用时经常有多种含义。Android 平台提供两种开发工具包，Android SDK 和 NDK。 SDK 是基于Java和Kotlin的程序语言，主要用来开发业务应用。NDK 是一个可直接访问底层 API(比如 OpenGL)的 C和C++ 的开发工具包，可用来开发底层的二进制库。这些库可被包含在使用 SDK 构建的应用内。所以，当我们在讨论 Android Native 应用时(比如, 基于SDK构建) 可能包含使用 NDK 构建 Native 代码。

Native 应用最大的缺点是只针对特定平台。在 Android 和 iOS平台上开发同一个应用需要维护两套独立的代码, 或引入复杂的开发工具才能将单套代码库移植到两个平台。以下的几个框架允许你通过编译一套代码到 Android 和 iOS两个平台上。

* [Xmarin]()
* [Google Flutter]()
* [React Native]()

使用这些框架开发的应用内部使用系统的 Native API，并提供跟 Native应用 相似的性能。所以，这些应用能使用所有设备的功能，包括 GPS，加速度计，相机，通知系统等。由于最终输出跟上面讨论的 Native 应用很相似，应用开发也会考虑使用这些框架来开发 Native 应用。

## Web 应用
手机 web 应用(简称 web 应用) 是设计上看起来和感觉上像 Native 应用的网站。这些应用使用 HTML5 技术开发运行在手机浏览器上，非常像现代网页。可以在桌面上创建启动图标，非常像访问 Native 应用；然而, 这些图标实际上关联的是浏览器标签，点击启动时打开系统默认浏览器并加载对应的 web 页面。

web 应用运行在浏览器中设备上的很多Native组件使用会被限制并且相比 Native 应用来说性能也更差。由于单个 web 应用的目标是多个平台，他们的设计规范不会跟着平台走。最大的优势是多个平台只需要维护一套代码并且发布更新时无需针对特定平台的应用商店。比如，对 web 应用中 HTML 文件更改后即可跨平台更新并运行而基于应用商城的更新则多依赖于商城。
## Hybrid 应用
Hybrid 应用试图中和 Native 和 web 应用各自的特点。 虽然 Hybrid 应用运行起来像 Native 应用，但实际上主要进程依赖于 web 技术，意味着应用的大部分功能运行在嵌入的浏览器里面(也叫 webview)。因此，Hybrid 应用继承了 Native 和 web 应用各自的优缺点。

一个 web-to-native 抽象层允许 Hybrid 应用访问纯 web 应用所不具备的设备原生功能。依赖使用框架开发，一套代码可运行在多个平台上，其用户界面与原生系统的用户界面非常相似。

以下几个是最流行的开发 Hybrid 应用的框架:

* [Apache Cordova]()
* [Framework 7]()
* [Ionic]()
* [jQuery Mobile]()
* [Native Script]()
* [Onsen UI]()
* [Sencha Touch]()

## Progressive Web 应用
Progressive Web 应用(PWA) 加载像正常的 web 页面, 但与通常的 web 应用在几个方面有所不同。比如可以离线试用和访问手机设备的硬件，这些功能通常只有 Native 应用才具备。

PWAs 结合了现代浏览器提供的不同的 web 开发标准以提供丰富的手机体验。一个 JSON 格式的应用清单文件中定义了该应用安装后具有哪些功能。

PWAs 支持 Android 和 iOS，但不是所有硬件功能都具备。比如系统通知，iPhone X 上的脸部识别 和 iOS 中所有的 ARKit 中增场现实功能 都不支持。PWA 对不同平台的支持性可在 [Medium article from Maximiliano Firtman]() 描述文件中查询到。
## 手机测试指南应用范围
在指南中，我们专注于Android 和 iOS的智能手机上运行的应用。这些平台主导当前市场也运行在其他类型设备包含平板电脑，智能手表，智能电视，自动驾驶汽车，及其他嵌入式系统。即使这些额外的设备超出了范围，你仍可以使用指南中绝大多数的知识和测试技术但不同的目标设备会有一些偏差。

鉴于存在大量可用的手机应用框架，不可能覆盖到这些所有框架。所以，我们专注于各个操作系统上的 Native 应用。然后，这些技术同样适用于 Hybrid 和 web 应用(毕竟，不管什么框架，所有应用都是基于 Native 组件)。