# Pango's Maven Repository

https://pango853.github.io/mvnrepo/index.html


# Acknowledgements
[ひしだま](http://www.ne.jp/asahi/hishidama/home/tech/index.html)さんが作成したMavenリポジトリーを参考に作ってみました。

REF: [ひしだまさんのMavenリポジトリー](http://hishidama.github.io/mvnrepository/)


# Introduction
Here are all the Hinemos dependent artifacts you may need for building or developing Hinemos.
They are not yet available in the central Maven repository so I created this repository to provide convenience to those who are interested in developing Hinemos like me.

主にHinemosの開発にあたって、関連や依存アーカイブを置くつもりのMavenリポジトリーです。


# HOWTO
build.gradleに以下のようにリポジトリを追加すれば利用可能。

    # build.gradle
    springVersion = "6.1.2"
    
    repositories {
        maven { url 'https://pango853.github.io/mvnrepo' }
    }
    
	dependencies {
		compile group: 'info.hinemos', name: 'hinemos-common', version: hinemos.version
		compile group: 'info.hinemos', name: 'hinemos-client-ws', version: hinemos.version
		compile group: 'info.hinemos', name: 'hinemos-agent-ws', version: hinemos.version
	}

# References
Regarding Hinemos, please refer to their official GitHub project page for more details.

アーカイブはHinemos本家のプロジェクトサイトをご覧下さい。

* [Hinemos GitHub page](https://github.com/hinemos/hinemos)
