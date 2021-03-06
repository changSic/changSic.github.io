---
layout: post
title:  "Custom Category TabBar Project"
date:   2019-07-16
excerpt: "Category TabBar 를 추상화 시켜서 어디든 재사용 할 수 있게 만들어보자!
"
tag:
- iOS
- OpenSource
comments: true
project: true
---

# Custom Category TabBar
mady by **Sicc**
* [Gutgub](https://github.com/changSic)

<a href="https://img.shields.io/badge/Version-v1.0-success"><img src="https://img.shields.io/badge/Version-v1.0-success"></a>
<a href="https://img.shields.io/badge/License-MIT-blue"><img src="https://img.shields.io/badge/License-MIT-blue"></a>
<a href="https://img.shields.io/badge/Platform-iOS-lightgrey"><img src="https://img.shields.io/badge/Platform-iOS-lightgrey"></a>
<a href="https://img.shields.io/badge/Swift-5.0-orange"><img src="https://img.shields.io/badge/Swift-5.0-orange"></a>

* Custom Category TabBar created using CollectionViews, Callback and Inheritance. Dynamic AutoLayout is applied to various iOS devices.

* CollectionView, Callback 그리고 상속을 활용해서 구현한 커스텀 카테고리 탭바. 다이나믹 오토레이아웃을 적용했기 때문에 iOS의 다양한 기기에 적용 가능한 커스텀 UI.

* [Features](#features)
* [Usage](#usage)
* [Examples](#examples)
* [Authors](#authors)
* [Contributors](#contributors)
* [License](#license)

# <a id="features">Features</a>
<figure class="third">
	<img src="/assets/ViewSwipe.gif">
	<img src="/assets/CategoryTap.gif">
	<img src="/assets/CategoryScrollingWithIndicatorBar.gif">
	<figcaption>If you scroll the category, IndicatorBar follows the category</figcaption>
</figure>

---

<a href="#eng">In English</a>

# <a id="usage">Usage</a>

### 언어 선택

* [English](#eng)

* [한국어로 보기](#kor)

---

<a id="eng"><strong>In English</strong></a>

* 1. DownLoad My [DemoProject](https://github.com/changSic/CustomCategoryTabBar)

* 2. Copy `CustomCategoryTabBar`Folder and Paste this file into your Project
<figure>
<a href="/assets/CategoryTabBarPath1.png">
<img src="/assets/CategoryTabBarPath1.png">
</a>
</figure>
<figure>
<a href="/assets/CategoryTabBarPath2.png">
<img src="/assets/CategoryTabBarPath2.png">
</a>
</figure>
<figure>
<a href="/assets/CustomCategoryTabBarFolder.png">
<img src="/assets/CustomCategoryTabBarFolder.png">
</a>
</figure>


* 3. Inherit `CategoryTabBarViewController` on the ViewController you will use
(this case is `DemoViewController`)
<figure>
<a href="/assets/InheritCategoryTabBarVC.png">
<img src="/assets/InheritCategoryTabBarVC.png">
</a>
</figure>

* 4. When you initialize the ViewController, you need to enter three parameters, and the last parameter is optional.
  * The first two params are `withTitles` and `withViews`.
  * The last param is `withScrollOption` and default is **true**
<figure>
<a href="/assets/CategoryTabBarInit.png">
<img src="/assets/CategoryTabBarInit.png">
</a>
</figure>

* 5. (Optional) The last parameter is an option for whether the category can be scrolled.
The image below is a true option, so you can scroll through the categories.
<img src="/assets/CategoryScrollingWithIndicatorBar.gif">


# <a id="examples">Examples</a>

### If you need
* ### 2 categories and Category Name is `First` and `Second`, Your code is like this

~~~ swift
let vc = DemoViewController(withTitles: ["First", "Second"],
                               withViews: [FirstDemoView(), SecondDemoView()])
~~~

<figure>
<a href="/assets/CategoryNumIs2.gif">
<img src="/assets/CategoryNumIs2.gif">
</a>
</figure>

* ### 4 categories and Category Name is `Hi` and `My` and `name` and `is`, Your code is like this
~~~ swift
let vc = DemoViewController(withTitles: ["Hi", "My", "Name", "is"],
                               withViews: [FirstDemoView(), SecondDemoView(), ThirdDemoView(), FourthDemoView()])
~~~
<figure>
<a href="/assets/CategoryNumIs4.gif">
<img src="/assets/CategoryNumIs4.gif">
</a>
</figure>

---

<a id="kor">한국어로 보기</a>

# Usage
* 1. DemoProject 를 다운로드 합니다.

* 2. `CustomCategoryTabBar`Folder 를 복사하고 자신의 프로젝트에 붙여넣기를 합니다!
<figure>
<a href="/assets/CategoryTabBarPath1.png">
<img src="/assets/CategoryTabBarPath1.png">
</a>
</figure>
<figure>
<a href="/assets/CategoryTabBarPath2.png">
<img src="/assets/CategoryTabBarPath2.png">
</a>
</figure>
<figure>
<a href="/assets/CustomCategoryTabBarFolder.png">
<img src="/assets/CustomCategoryTabBarFolder.png">
</a>
</figure>


* 3. 이 기능을 사용할 자신  View Controller 에 `CategoryTabBarViewController` 를 상속받습니다. (아래의 경우에는 `DemoViewController` 가 될 것.)
<figure>
<a href="/assets/InheritCategoryTabBarVC.png">
<img src="/assets/InheritCategoryTabBarVC.png">
</a>
</figure>

* 4. ViewController 를 초기화 할 때, 3개의 매개변수를 입력해야 하고 마지막 매개변수는 선택사항 입니다.
  * 처음 두 개의 인자는 `withTitles` 과 `withViews` 입니다
  * 마지막 인자는 `withScrollOption` 이고 기본값이 **true** 입니다.
<figure>
<a href="/assets/CategoryTabBarInit.png">
<img src="/assets/CategoryTabBarInit.png">
</a>
</figure>

* 5. (선택사항) 마지막 인자는 카테고리가 스크롤이 가능한지에 대한 옵션입니다. 아래 사진에서는 true 옵션에 해당하는 것이어서 카테고리가 스크롤 됨을 볼 수 있습니다.

<img src="/assets/CategoryScrollingWithIndicatorBar.gif">



# Examples

### 사용자가 만약
* **2 개의 카테고리** 를 사용하고 카테고리 이름이 `First` 과 `Second` 이면, 코드는 아래와 같습니다.
~~~ swift
let vc = DemoViewController(withTitles: ["First", "Second"],
                               withViews: [FirstDemoView(), SecondDemoView()])
~~~
<figure>
<a href="/assets/CategoryNumIs2.gif">
<img src="/assets/CategoryNumIs2.gif">
</a>
</figure>

* **4 개의 카테고리** 를 사용하고 카테고리 이름이 `Hi`, `My`, `name`,  `is` 이면, 코드는 아래와 같습니다.
~~~ swift
let vc = DemoViewController(withTitles: ["Hi", "My", "Name", "is"],
                               withViews: [FirstDemoView(), SecondDemoView(), ThirdDemoView(), FourthDemoView()])
~~~
<figure>
<a href="/assets/CategoryNumIs4.gif">
<img src="/assets/CategoryNumIs4.gif">
</a>
</figure>

---

# <a id="author">Author</a>
**Sicc**. I'm Student of South Korea studying Programming

* [Gutgub](https://github.com/changSic)
* [Blog](https://changsic.github.io/)
* [Portfolio](https://changsic.github.io/AboutSicc/)

# <a id="contributors">Contributors</a>
Thanks to everyone kind enough to submit a pull request.

# <a id="license">MIT License</a>

	Copyright (c) 2017 Andrea Mazzini. All rights reserved.

	Permission is hereby granted, free of charge, to any person obtaining a
	copy of this software and associated documentation files (the "Software"),
	to deal in the Software without restriction, including
	without limitation the rights to use, copy, modify, merge, publish,
	distribute, sublicense, and/or sell copies of the Software, and to
	permit persons to whom the Software is furnished to do so, subject to
	the following conditions:

	The above copyright notice and this permission notice shall be included
	in all copies or substantial portions of the Software.

	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
	OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
	MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
	IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
	CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
	TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
	SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
