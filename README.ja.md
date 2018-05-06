# gradle-kotlin-multiprojects-template

GradleでKotlinを用いたマルチプロジェクト型レイアウトのテンプレートです。

## 使い方

GitHub上の`Clone or download`ボタンから、このリポジトリをzip形式でダウンロードし、展開します。展開後のディレクトリ名は、任意のものに変更してください。  
次にIntelliJ IDEAなどのIDEでディレクトリをインポートします。以上で完了です。

## プロジェクト名の変更方法
`/settings.gradle`を開き、`rootProject.name`プロパティを任意のプロジェクト名に変更してください。

## サブプロジェクト名 (`subproject1`) の変更方法

`/settings.gradle`を開き、`include`に続く文字列を任意のサブプロジェクト名へ変更します。  
続いて同様に、`/subproject`ディレクトリを`include`で変更したサブプロジェクト名と同一に変更してください。

## GroupId (`com.example`) の変更方法

`/build.gradle`を開き、`buildscript > ext > projectVersions > group`の内容を変更します。  
続いて`/subproject1/src/main/java/com/example/Main.kt`を開き、先頭の`package com.example`の記述を当該のものに変更します。  
最後に`/subproject1/src/{main, test}/{java, kotlin}`内のディレクトリ構造を当該のものに変更してください。

## Mainクラスの変更方法

`/subproject1/build.gradle`を開き、`mainClassName`プロパティを変更してください。

## JDKバージョンの変更方法

`/build.gradle`を開き、`subprojects > tasks.withType(JavaCompile)`内の各プロパティを変更します。  
続いて`/subproject1/build.gradle`を開き、`dependencies`内の`org.jetbrains.kotlin:kotlin-stdlib-jdk8`を置き換えてください。

たとえば、JDK7を利用したい場合は`org.jetbrains.kotlin:kotlin-stdlib-jdk7`です。

## Kotlinバージョンの変更方法

`/build.gradle`を開き、 `buildscript > ext > versions > kotlin`の内容を変更してください。
