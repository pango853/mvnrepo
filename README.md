# Pango's Maven Repository

https://pango853.github.io/mvnrepo/index.html


# Acknowledgements
[ひしだま](http://www.ne.jp/asahi/hishidama/home/tech/index.html)さんが作成したMavenリポジトリーを参考に作ってみました。

REF: [ひしだまさんのMavenリポジトリー](http://hishidama.github.io/mvnrepository/)


# Introduction
Here are all the Hinemos dependent artifacts you may need for building or developing Hinemos.
They are not yet available in the central Maven repository so I created this repository to provide convenience to those who are interested in developing Hinemos like me.

主にHinemosの開発にあたって、関連や依存アーカイブを置くつもりのMavenリポジトリーです。


# HOW-TO
build.gradleに以下のようにリポジトリを追加すれば利用可能。

	# build.gradle
	hinemosVersion = '6.1.2'

	repositories {
		maven { url 'https://pango853.github.io/mvnrepo' }
	}
	
	dependencies {
		compile group: 'info.hinemos', name: 'hinemos-common', version: hinemosVersion
		compile group: 'info.hinemos', name: 'hinemos-client-ws', version: hinemosVersion
		compile group: 'info.hinemos', name: 'hinemos-agent-ws', version: hinemosVersion
	}


# EXTEND THIS WORK

> cd mvnrepo

> mkdir TMP\extracted\

Download, install if needed, and then copy JAR files to TMP\extracted\

> mvn install:install-file -Dfile=TMP\extracted\HinemosCommon.jar -DgroupId=info.hinemos -DartifactId=hinemos-common -Dversion=5.0.4 -Dpackaging=jar -DlocalRepositoryPath=.

> mvn install:install-file -Dfile=TMP\extracted\HinemosManager.jar -DgroupId=info.hinemos -DartifactId=hinemos-manager -Dversion=5.0.4 -Dpackaging=jar -DlocalRepositoryPath=.
> mvn install:install-file -Dfile=TMP\extracted\HinemosModel.jar -DgroupId=info.hinemos -DartifactId=hinemos-model -Dversion=5.0.4 -Dpackaging=jar -DlocalRepositoryPath=.
> mvn install:install-file -Dfile=TMP\extracted\HinemosManagerCli.jar -DgroupId=info.hinemos -DartifactId=hinemos-manager-cli -Dversion=5.0.4 -Dpackaging=jar -DlocalRepositoryPath=.

> mvn install:install-file -Dfile=TMP\extracted\AgentWS.jar -DgroupId=info.hinemos -DartifactId=agent-ws -Dversion=5.0.4 -Dpackaging=jar -DlocalRepositoryPath=.
> mvn install:install-file -Dfile=TMP\extracted\HinemosAgent.jar -DgroupId=info.hinemos -DartifactId=hinemos-agent -Dversion=5.0.4 -Dpackaging=jar -DlocalRepositoryPath=.

> mvn install:install-file -Dfile=TMP\extracted\HinemosClient.jar -DgroupId=info.hinemos -DartifactId=hinemos-client -Dversion=5.0.4 -Dpackaging=jar -DlocalRepositoryPath=.
> mvn install:install-file -Dfile=TMP\extracted\ClientWS.jar -DgroupId=info.hinemos -DartifactId=client-ws -Dversion=5.0.4 -Dpackaging=jar -DlocalRepositoryPath=.



# References
Regarding Hinemos, please refer to their official GitHub project page for more details.

アーカイブはHinemos本家のプロジェクトサイトをご覧下さい。

* [Hinemos GitHub page](https://github.com/hinemos/hinemos)
