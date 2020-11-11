# iOSの環境構築について
アプリのチーム開発の一つの壁として、環境構築があると思います。なるべく早い段階でクリアしていたほうが良いため、ドラフトではありますが、使うであろうライブラリやツールなどを挙げておきます。

## 最低限必要なツール
チーム開発において、コンフリクトを最小限かつリソース共有化は必須ですが、そのためのツールとして割いて現必要なものを以下に挙げます。（個人的に必要だと思っているものですが）
* XcodeGen -> Projectファイルをyamlから生成するツール。.pbxprojでコンフリクトするのを防ぐ
[GitHub - yonaskolb/XcodeGen: A Swift command line tool for generating your Xcode project](https://github.com/yonaskolb/XcodeGen)
* fastlane -> アプリのデプロイや、証明書管理をする時に使います
[GitHub - fastlane/fastlane: 🚀 The easiest way to automate building and releasing your iOS and Android apps](https://github.com/fastlane/fastlane)
* Carthage -> ライブラリ管理のSwiftコマンドラインツール
[GitHub - Carthage/Carthage: A simple, decentralized dependency manager for Cocoa](https://github.com/Carthage/Carthage)
*  mint -> Swift製のライブラリ管理ツール
[GitHub - yonaskolb/Mint: A package manager that installs and runs executable Swift packages](https://github.com/yonaskolb/Mint)
* Genesis -> テンプレートからファイルを自動生成するツール
[GitHub - yonaskolb/Genesis: Templating, scaffolding and generation tool](https://github.com/yonaskolb/Genesis)
## 必要なライブラリ
### Rxに関連するライブラリ
最近のアプリ開発では、デファクトスタンダードになりつつ（なっている？）Reactive Extensionsを使えるようにするためのライブラリ
以下の二つのどちらか採用
* RxSwift -> Reactive Extensionsで開発するためのライブラリ（一般的）
[GitHub - ReactiveX/RxSwift: Reactive Programming in Swift](https://github.com/ReactiveX/RxSwift)
* Combine -> 純正のRxライブラリ iOS13以降から使える（これから一般的になるであろうライブラリ）
[Combine swift - Google 検索](https://www.google.com/search?sxsrf=ALeKk026xwaVBIS2cXM6Xnf6RlWYlBj6Vw%3A1605105402009&ei=-varX5kKz-bBA7eDvZAL&q=Combine+swift&oq=Combine+swift&gs_lcp=CgZwc3ktYWIQAzICCAAyAggAMgIIADIFCAAQywEyBQgAEMsBMgUIABDLATIFCAAQywEyBQgAEMsBOgQIABBHOgQIABAEULUYWLofYJkgaABwAngAgAHiAYgBqAaSAQUwLjQuMZgBAKABAaoBB2d3cy13aXrIAQjAAQE&sclient=psy-ab&ved=0ahUKEwiZ78DK2_rsAhVPc3AKHbdBD7IQ4dUDCA0&uact=5)

## アーキテクチャ
僕が書けるアーキテクチャは以下のもの
* Kickstarter MVVM
* Clean Architecture
* MVVM + Redux

### スピード感
Kickstarter MVVM > MVVM + Redux > Clean Architecture 

### 関心の分離度（多分あってるはず）
Clean Architecture > MVVM + Redux > Kickstarter MVVM
