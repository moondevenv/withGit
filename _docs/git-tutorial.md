# Git의 기본

## [시작하기](https://backlog.com/git-tutorial/kr/intro/intro1_1.html)

안녕, 하카타에서 태어난 원숭이 킥킥이야. 오늘은 나랑 같이 버전 관리 시스템, 'Git(깃)' 을 공부해보자.

여러분은 파일을 편집 전 상태로 되돌리고 싶을 때 어떻게 하고 있나요?

가장 간단한 방법은 편집하기 전에 파일을 미리 복사해두는 것입니다. 파일과 폴더명 뒤에 편집한 날짜를 붙여주는 방식이죠. 하지만 파일을 편집할 때마다 매번 복사하는 일은 번거롭기도 하고 실수할 가능성도 많습니다.

![파일 백업의 예](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_1_1.png)

또한 위의 그림처럼 특별한 규칙 없이 마음대로 이름을 붙여놓는 경우 어느 파일이 최신인지, 또 파일의 어떤 부분이 변경된 것인지 파악하기 어렵습니다.

아래 그림을 보세요. 이렇게 여러 명이 공유한 파일을 동시에 편집하는 바람에 다른 사람이 먼저 변경하고 있던 내용을 지워버린 경험은 없나요?

![팀 작업의 실패 사례](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_1_2.png)

바로 이런 문제를 해결하기 위해 만들어진 것이 Git과 같은 버전 관리 시스템입니다.

### Git을 이용하여 버전 관리하기

Git이란 소스코드를 효과적으로 관리하기 위해 개발된 '분산형 버전 관리 시스템'입니다. 원래는 Linux 소스코드를 관리할 목적으로 개발 되었습니다.

Git에서는 소스 코드가 변경된 이력을 쉽게 확인할 수 있고, 특정 시점에 저장된 버전과 비교하거나 특정 시점으로 되돌아갈 수도 있습니다.

또 내가 올리려는 파일이 누군가 편집한 내용과 충돌한다면, 서버에 업로드 할 때 경고 메시지가 발생됩니다. 누군가가 애써 편집한 내용을 덮어써버리는 실수는 이제 없겠죠!

![팀 작업에 버전관리 활용하기](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_1_3.png)

Git으로 파일을 관리하면, 업데이트 이력이 Git에 저장되지.

매번 백업용 파일 복사본을 만들 필요가 없으니까 엄청 편하고 깔끔하다구!

---

## [이력을 관리하는 저장소](https://backlog.com/git-tutorial/kr/intro/intro1_2.html)

저장소(Git repository)란 말그대로 파일이나 폴더를 저장해 두는 곳입니다. 그런데 Git 저장소가 제공하는 좋은 점 중 하나는 파일이 변경 이력 별로 구분되어 저장된다는 점입니다. 비슷한 파일이라도 실제 내용 일부 문구가 서로 다르면 다른 파일로 인식하기 때문에 파일을 변경 사항 별로 구분해 저장할 수 있습니다.

![파일과 폴더 이력을 관리하는 저장소](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_2_1.png)

### 원격 저장소와 로컬 저장소

Git은 원격 저장소와 로컬 저장소 두 종류의 저장소를 제공합니다.

- 원격 저장소(Remote Repository): 파일이 원격 저장소 전용 서버에서 관리되며 여러 사람이 함께 공유하기 위한 저장소입니다.
- 로컬 저장소(Local Repository): 내 PC에 파일이 저장되는 개인 전용 저장소입니다.

평소에는 내 PC의 로컬 저장소에서 작업하다가 작업한 내용을 공개하고 싶을 때에 원격 저장소에 업로드 합니다. 물론 원격 저장소에서 다른 사람이 작업한 파일을 로컬 저장소로 가져올 수도 있습니다.

![원격 저장소와 로컬 저장소](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_2_2.png)

### 저장소 만들기

내 컴퓨터에 로컬 저장소를 만드는 방법은 두 가지가 있습니다.

첫 번째, 아예 저장소를 새로 만들거나, 두번째, 이미 만들어져 있는 원격 저장소를 로컬 저장소로 복사해 올 수 있습니다.

![저장소 만들기](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_2_3.png)

다음 페이지에서는 커밋이란걸 알려줄게!

----

## [변경을 기록하는 커밋](https://backlog.com/git-tutorial/kr/intro/intro1_3.html)

파일 및 폴더의 추가/변경 사항을 저장소에 기록하려면 '커밋'이란 버튼을 눌러줘야 합니다.

커밋 버튼을 누르면 이전 커밋 상태부터 현재 상태까지의 변경 이력이 기록된 커밋(혹은 리비전)이 만들어집니다.

커밋은 아래 그림처럼 시간순으로 저장됩니다. 최근 커밋부터 거슬러 올라가면 과거 변경 이력과 내용을 알 수 있겠죠.

![시간순으로 저장된다.](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_3_1.png)

각 커밋에는 영문/숫자로 이루어진 40자리 고유 이름이 붙습니다. 저장소에선 이 40자리 이름을 보고 각 커밋을 구분하고 선택합니다.

Tips

버그 수정, 기능 추가 등 특별한 의미가 있는 업데이트를 작업 별로 구분해서 각각 커밋하면, 나중에 이력을 보고 특정 변경 내용을 찾기 쉽습니다.

커밋은 이렇게 이력을 남기는 중요한 작업이기 때문에 커밋 버튼을 누를땐 커밋 메시지를 필수로 입력해야 합니다. 메시지가 없으면 커밋이 실행되지 않습니다.

Tips

메시지는 명료하고 이해하기 쉽게 남겨야 본인 뿐만 아니라 다른 사람이 커밋 이력을 확인하기 쉽습니다. Git 에서 권장하는 메시지 형식을 따르는 것도 좋습니다.

1번째 줄 : 커밋 내의 변경 내용을 요약
2번째 줄 : 빈 칸
3번째 줄 : 변경한 이유

주로 위 형식으로 메시지를 작성합니다.

----

## [작업 트리(Work tree)와 인덱스(Index)](https://backlog.com/git-tutorial/kr/intro/intro1_4.html)

Git 에서는 우리가 흔히 말하는 폴더를 '작업 트리'(Work Tree)라고 부릅니다.

그리고 커밋을 실행하기 전의 저장소와 작업 트리 사이에 존재하는 공간을 '인덱스'라고 합니다.

![작업 트리(Work tree)와 인덱스(Index)](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_4_1.png)

지금까지 배운 Git 용어를 총정리 해 볼까요?

Git의 '커밋' 작업은 '작업 트리'에 있는 변경 내용을 저장소에 바로 기록하는 것이 아니라 그 사이 공간인 '인덱스'에 파일 상태를 기록(stage - 스테이징 한다고 표현하기도 합니다)하게 되어 있습니다. 따라서 저장소에 변경 사항을 기록하기 위해서는, 기록하고자 하는 모든 변경 사항들이 '인덱스'에 존재해야 합니다.

예를 들어, 10개의 파일을 수정했지만 그 중에 7개만 저장소에 공개하고 싶을 때를 생각해 보세요. 변경한 10개의 파일 중 7개를 선택하는 작업이 바로 '인덱스에 등록' 또는 '스테이징(stage)'이라 표현하는 작업 입니다.

이렇게 인덱스란 공간(가상이지만요!)이 중간에 있는 덕분에 작업 트리 안에 있는 커밋이 필요 없는 파일들을 커밋에 포함하지 않을 수 있고, 파일에서 내가 원하는 일부 변경 사항만 인덱스에 등록해 커밋할 수 있습니다.

자, 다음 페이지에선 지금까지 배운 내용을 직접 실습해보자! 실제로 Git을 설치해서 프로젝트에 참여해 보는거야!

----

# 튜토리얼 1: Git의 기본

## [Git 설치](https://backlog.com/git-tutorial/kr/intro/intro2_1.html)

실습에 들어가기 전에, 우선 Git을 이용하기 위한 환경을 구축, 총 3가지 환경 - Windows(GUI), Mac(GUI), 콘솔(커맨드 라인) - 으로 나누어 설명을 진행하겠습니다.

개발자 분이나 콘솔 환경에 익숙한 분은 콘솔을 이용해 Git 에 도전해 보세요.

### Windows

여기서는 오픈소스 Git 클라이언트 'TortoiseGit'과 그 언어팩까지 설치해 보겠습니다.
[http://code.google.com/p/tortoisegit/](http://code.google.com/p/tortoisegit/)

Tips

TortoiseGit을 이용하려면, 먼저 msysgit를 설치해야 합니다. 아래 사이트에서 설치파일을 다운로드합니다.
[http://msysgit.github.io/](http://msysgit.github.io/)

그리고 아래 사이트에서 TortoiseGit 설치파일과 언어팩을 다운로드합니다. 32비트판과 64비트판을 구분하고 있으니 내 Windows 환경에 맞게 선택하세요.

![TortoiseGit을 다운로드](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_1_win.png)

다운로드한 설치 파일을 더블클릭합니다. 지금부턴 무조건 Next를 클릭합니다.

![TortoiseGit ](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_4_win.png)

Next를 클릭합니다.

![Next를 클릭](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_5_win.png)

TortoisePLink를 선택한 상태로 Next를 클릭합니다.

![TortoisePLink를 선택한 상태로, Next를 클릭](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_6_win.png)

Next를 클릭합니다.

![이대로 Next를 클릭](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_7_win.png)

Install을 클릭합니다.

![Install을 클릭](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_8_win.png)

설치가 시작됩니다. 사용자 인증이 필요한 경우에는 인증을 진행해주세요.

![설치가 시작됩니다](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_9_win.png)

설치가 완료됐습니다. Finish를 클릭해 종료해주세요.

![설치 완료](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_10_win.png)

이어서 언어팩을 적용합니다.
Language Packs에서 Korean를 다운로드하고 더블 클릭해서 시작합니다. Next를 클릭합니다.

![Language Packs에서 Korean를 다운로드](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_11_win.png)

설치가 시작됩니다. 사용자 인증이 필요한 경우에는 인증을 진행해주세요.

![설치가 시작됩니다](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_12_win.png)

설치가 완료됐습니다. Finish를 클릭해 종료해주세요.

![설치 완료](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_13_win.png)

데스크톱의 적당한 곳에 우클릭 메뉴를 표시하세요. Git의 메뉴 항목이 추가되어 있을테니, TortoiseGit > Settings를 클릭해주세요.

![우클릭 메뉴에 Git 메뉴 항목이 추가](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_14_win.png)

설정 화면이 표시됩니다. General 화면의 Language에서 한국어를 선택한 후 OK를 클릭해주세요.

![General 화면의 Language에서 한국어를 선택](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_1_15_win.png)

드디어 설치와 한국어 설정이 끝났습니다.

----

## [초기 설정](https://backlog.com/git-tutorial/kr/intro/intro2_2.html)

설치한 Git에 본인의 사용자명과 메일 주소를 등록해주세요. 여기서 설정한 사용자 정보는 나중에 변경 이력 등에 표시됩니다.

### Windows

마우스 우클릭해서 메뉴> TorotiseGit> 설정으로 들어갑니다.

![TortoiseGit의 설정을 클릭](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_2_2_win.png)

설정화면이 표시됩니다. Git의 화면에서 User Info란에 사용자명과 메일을 입력해주세요.

![Git의 화면에서 유저 정보의 이름과 메일을 입력](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_2_3_win.png)

이걸로 기본 환경설정은 끝! 다음 페이지에서는 저장소를 만들어보자!

----

## [새 저장소 만들기](https://backlog.com/git-tutorial/kr/intro/intro2_3.html)

먼저 로컬에「tutorial」이라는 이름으로 빈 폴더를 만들어 로컬 저장소로 등록해 봅시다.

이후 튜토리얼은 이 폴더를 이용해 진행하겠습니다.

### Windows

우선 tutorial 폴더를 아무데나 생성해주세요. tutorial 폴더를 Git 관리 하에 두려면, 폴더 안 빈 화면에서 우클릭을 한 후 「Git 이곳에 저장소를 작성」을 클릭합니다.

![Git 여기에 저장소를 작성」을 클릭](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_3_1_win.png)

아래 화면이 보이면 바로 OK 버튼을 클릭하세요.(만약 Bare에 체크하면 단순히 Push된 변경내역만 보이게 됩니다. PC에서 웹 상과 동일한 모든 작업을 하려면 체크하지 않고 넘어가세요.)

![저장소 작성](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_3_2_win.png)

성공하면 다음과 같은 화면이 표시됩니다. OK 버튼을 클릭하고 닫아주세요.

![작성 성공 화면](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_3_3_win.png)

tutorial 폴더 아이콘에 다음과 같이 초록색 체크 배지가 달리게 됩니다. 아이콘 표시가 바뀌지 않으면 우클릭 메뉴에서 「최신 상태로 업데이트」를 클릭해주세요.

![tutorial 폴더의 아이콘](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_3_4_win.png)

### Mac

우선 tutorial 폴더를 아무데나 생성해주세요.
그 후, Source Tree를 켭니다.

즐겨찾기 목록 화면의 왼쪽 위에 있는 Add Repository 버튼을 클릭합니다. 또는 메뉴바에서 파일>신규를 선택해주세요.

![Source Tree를 켬](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_3_1_mac.png)

저장소 생성 버튼을 클릭합니다.
로컬 저장소로 설정하는 폴더와, Source Tree상에서 표시하는 이름을 즐겨찾기명으로 입력해 작성 버튼을 클릭하세요.

여기에는 tutorial 폴더를 「tutorial」이라는 북마크명으로 등록했습니다.

![저장소를 작성](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_3_2_mac.png)

짜잔, 즐겨찾기 목록에 지금 추가한 저장소가 표시됐습니다.

![즐겨찾기 목록](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_3_3_mac.png)

### 콘솔

우선 tutorial 폴더를 아무데나 생성해주세요. tutorial 폴더를 Git의 저장소로 등록하려면, 해당 폴더로 이동하여 init 명령어를 사용합니다.

```bash
$ git init
```

여기서는, 새롭게 만든 tutorial 폴더를 Git 저장소로 설정했습니다.

```bash
$ mkdir tutorial
$ cd tutorial
$ git init
Initialized empty Git repository in /Users/yourname/Desktop/tutorial/.git/
```

이제 지금 만든 저장소에 파일을 커밋해보자!

----

## [파일 커밋(Commit)하기](https://backlog.com/git-tutorial/kr/intro/intro2_4.html)

tutorial 폴더에 새로운 파일을 추가하고, 원격 저장소에 파일을 등록해보세요.

우선 tutorial 폴더 안에 「sample.txt」라는 이름으로 텍스트 파일을 만드세요. 파일 내용에는 적당히 아래 텍스트를 입력하시면 됩니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
```

### 콘솔

Git의 관리 하에 있는 폴더의 작업트리와 인덱스 상태를 확인하려면, status 명령어를 사용합니다.

```bash
$ git status
```

status 명령어를 실행해 tutorial 폴더 상태를 확인합니다.

```bash
$ git status
## On branch master
#
## Initial commit
#
## Untracked files:
##   (use "git add <file>..." to include in what will be committed)
#
##     sample.txt
nothing added to commit but untracked files present (use "git add" to track)
```

이력 추적 대상이 되지 않은 파일(untracked files)로, sample.txt가 보이네요. 처음 한번만 인덱스에 등록하면 추적 대상으로 등록할 수 있습니다.

파일을 인덱스에 등록하는 명령어는 add 입니다. 뒤에 <file>을 붙여 인덱스에 등록할 파일을 지정합니다. 한칸 띄어쓰기해서 여러개 파일을 한번에 지정할수도 있습니다.

```bash
$ git add <file>..
```

Tips

파라미터에 「.」를 지정하면, 모든 파일을 인덱스에 등록할 수 있습니다.

```bash
$ git add .
```

그럼 sample.txt를 인덱스에 추가하여 확인해보겠습니다.

```bash
$ git add sample.txt
$ git status
## On branch master
#
## Initial commit
#
## Changes to be committed:
##   (use "git rm --cached <file>..." to unstage)
#
##     new file:   sample.txt
#
```

인덱스에 sample.txt가 추가되었으니 커밋 준비는 끝입니다. 이제 commit 명령어를 실행해 커밋을 진행합니다. commit 명령어 포맷은 다음과 같습니다.

```bash
$ git commit -m "<댓글>"
```

commit 명령어를 실행한 후 상태를 확인합니다.

```bash
$ git commit -m "first commit"
[master (root-commit) 116a286] first commit
 0 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 sample.txt

$ git status
## On branch master
nothing to commit (working directory clean)
```

이제 모든 변경사항이 커밋되었습니다.

저장소의 변경 이력을 확인해봅시다. 저장소 변경 이력을 보려면, log 명령어를 사용하세요.

```bash
$ git log
commit ac56e474afbbe1eab9ebce5b3ab48ac4c73ad60e
Author: eguchi <eguchi@nulab.co.jp>
Date:   Thu Jul 12 18:00:21 2012 +0900

    first commit
```

Note

git를 설치할 때 gitk라는 툴도 동시에 설치됩니다. 이걸 사용하면 변경 이력을 GUI에서 확인할 수 있습니다.

```bash
$ gitk
```

![gitk ](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro2_4_1_cui.png)

이제 저장소를 다른 작업자와 공유하는 방법에 대해 설명해볼게요!

----

# 저장소 공유하기

## [원격 저장소에 푸시(Push)하기](https://backlog.com/git-tutorial/kr/intro/intro3_1.html)

지금까지는 로컬 저장소의 기본적인 사용 방법을 설명했습니다. 이제부터는 원격 저장소를 이용하여 로컬 저장소의 변경 이력을 공유하는 방법에 대해 알아 보겠습니다.

### push

내 PC의 로컬 저장소에서 변경된 이력을 원격 저장소에 공유하려면, 로컬 저장소의 변경 이력을 원격 저장소에 업로드해야 합니다.

웹 상의 원격 저장소로 변경된 파일을 업로드하는 것을 Git에서는 푸시(Push)라고 합니다. push 를 실행하면, 원격 저장소에 내 변경 이력이 업로드되어, 원격 저장소와 로컬 저장소가 동일한 상태가 됩니다.

![Push](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro3_1_1.png)

----

## [원격 저장소 복제(Clone)하기](https://backlog.com/git-tutorial/kr/intro/intro3_2.html)

누군가의 변경 이력이 적용된 원격 저장소가 있으면, 그걸 웹에서 통째로 복제해와 내 PC에서 직접 작업할 수 있습니다.

### clone

원격 저장소를 복제하려면, 클론(Clone)이라는 조작을 수행합니다.

복제란 원격 저장소의 내용을 통째로 다운로드하는 것을 말합니다. 복제한 저장소를 다른 PC에서 로컬 저장소로 사용할 수 있게 됩니다.

Note

변경 이력도 함께 로컬 저장소에 복제되어 오므로, 원래 원격 저장소와 똑같이 이력을 참조하고 커밋을 진행할 수 있습니다.

----

## [원격 저장소에서 풀(Pull)해오기](https://backlog.com/git-tutorial/kr/intro/intro3_3.html)

원격 저장소를 공유해 여러 사람이 함께 작업을 하면, 모두가 같은 원격 저장소에 푸시(Push)합니다. 그럼 다른 사람이 원격 저장소에 올려놓은(Push) 변경 내용을 내 로컬 저장소에도 적용(Pull)할 필요가 있습니다.

### Pull

원격 저장소에서 로컬 저장소로 업데이트하려면 풀(Pull)을 실행합니다.

pull 을 실행하면, 원격 저장소에서 최신 변경 이력을 다운로드하여 내 로컬 저장소에 그 내용을 적용합니다.

![Pull](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro3_3_1.png)

이제 본격적인 실습을 시작해볼까? Backlog의 원격 저장소를 이용해 저장소를 공유해보자구!

----

# 튜토리얼2 저장소 공유

## [Backlog에 원격 저장소 생성하기](https://backlog.com/git-tutorial/kr/intro/intro4_1.html)

우선은 원격 저장소를 Backlog 상에 만들어봅시다.

Tips

Backlog 에서는 관리자 권한이 있는 사용자만 Git 저장소를 만들 수 있습니다. 만약 관리자 권한을 가지고 있지 않으면 관리자 권한을 가지고 있는 사람에게 저장소 생성을 요청해야 합니다. 또는 무료 계정을 만들어(30일 동안 무료 사용 가능) Backlog 공간을 이용할 수도 있습니다.

[계정 만들려면 클릭](https://backlog.com/pricing/)

우선 Backlog에 로그인하여, 저장소를 만들 프로젝트 메뉴에서 「Git」을 클릭합니다. Git 을 만드려면 최소 1개의 프로젝트가 필요합니다.

![저장소를 작성하는 프로젝트에서 「Git」를 클릭](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro4_1_1.png)

상단 메뉴에서 Git 메뉴가 보이지 않을 경우, 프로젝트를 선택 후 「프로젝트 설정」 > 「Git 설정」 에서 Git 기능을 활성화시킵니다.

![Git 설정에서 Git 기능을 활성화하기](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro4_1_2.png)

Git 기능을 활성화 한 후, 동일한 Git의 설정 화면에서 「저장소를 추가한다」를 클릭합니다.

![「저장소를 추가한다」를 클릭](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro4_1_3.png)

「저장소 이름」과 「설명」을 입력해 「저장소를 작성한다」 버튼을 클릭합니다. 여기서는 이름에 「tutorial」, 설명에 「튜토리얼용입니다」라고 입력했습니다.

![「저장소명」과 「설명」을 입력해 「저장소를 작성한다」 버튼을 클릭](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro4_1_4.png)

아래 그림처럼 새로운 저장소가 추가되었습니다.

![새로운 저장소가 추가되었습니다](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro4_1_5.png)

이제 이 원격 저장소에 push 라는걸 해보자!

----

## [원격 저장소에 푸시(Push)하기](https://backlog.com/git-tutorial/kr/intro/intro4_2.html)

「튜토리얼 Git의 기본」에서 만든 로컬 저장소 「tutorial」를 push 해보세요.

### 콘솔

원격 저장소에 로컬 저장소의 이력을 push합시다.

원격 저장소의 주소는 이름으로 기록해 둘 수 있습니다. 기록 해두면 push 할 때마다 긴 원격 저장소의 주소를 입력 할 필요가 없습니다. 우선 「origin」이라는 이름으로 원격 저장소를 등록하고 push합니다.

원격 저장소를 추가하려면, remote 명령어를 사용합니다. <name>은 등록명, <url>은 원격 저장소의 URL을 지정합니다.

$ git remote add <name> <url>

다음 명령어를 실행해, 이전 페이지에서 만든 원격 저장소의 URL을 origin이라는 이름으로 등록합니다.

![원격 저장소의 URL을 origin이라는 이름으로 등록](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro4_2_1_cui.png)

$ git remote add origin _https://[your_space_id].backlogtool.com/git/[your_project_key]/tutorial.git_

Tips

콘솔일 경우 push 나 pull 은 실행 시에 원격 저장소명을 생략하면, origin이라는 이름의 원격 저장소를 사용합니다. 그 때문에 원격 저장소에는 origin이라는 이름을 붙이는 것이 일반적입니다.

저장소를 push 하려면, push 명령어를 사용합니다. <repository>는 push 경로의 주소, <refspec>은 push 할 브랜치를 지정합니다. 브랜치에 대한 내용은 발전편에 자세하게 설명이 나와 있습니다.

$ git push <repository> <refspec>...

다음 명령어를 실행해 원격 저장소 origin에 커밋을 push합니다. 실행 옵션에서 한번 -u를 지정하면, 이후에는 그 브랜치명 지정을 생략할 수 있습니다. 단, 비어있는 원격 저장소에 최초로 push했을 때는 원격 저장소명과 브랜치명을 생략할 수 없습니다.

도중에 사용자명과 비밀번호가 요구되면 Backlog의 사용자명과 비밀번호를 입력하십시오.

```bash
$ git push -u origin master
Username: <사용자명>
Password: <비밀번호>
Counting objects: 3, done.
Writing objects: 100% (3/3), 245 bytes, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://monkey.backlogtool.com/git/BLG/tutorial.git
 * [new branch]      master -> master
```

Backlog의 Git 페이지를 열어보세요. 최근 업데이트에 push 항목이 추가되어 있습니다.

![최근 업데이트에 push 항목이 추가](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro4_2_9.png)

저장소의 파일 목록에는, push한 저장소의 파일이 추가되었습니다.

![push한 저장소의 파일이 추가](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro4_2_10.png)

다음 페이지에서는 이 원격 저장소를 복제해보자!

----

## [원격 저장소 복제(Clone)하기](https://backlog.com/git-tutorial/kr/intro/intro4_3.html)

원격 저장소를 복제하여 다른 곳에서도 작업을 할 수 만들어 봅시다.

내가 다른 사용자가 됐다고 가정하고 아까 Push했던 원격 저장소의 파일을 내PC의 "튜토리얼2"라는 새폴더로 복사해 오겠습니다.

### 콘솔

저장소를 복제하려면 clone 명령어를 이용합니다. <repository>는 원격 저장소의 URL, <directory>는 복제대상의 폴더명을 지정합니다.

```bash
$ git clone <repository> <directory>
```

아래 명령을 실행하면, 현재 폴더에 tutorial2라는 이름의 폴더명에 원격 저장소가 복제됩니다.

```bash
$ git clone _https://monkey.backlogtool.com/git/BLG/tutorial.git_ tutorial2
Cloning into 'tutorial2'...
Username: <사용자명>
Password: <비밀번호>
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (3/3), done.
```

복제한 저장소 「tutorial」 안에, 아까 push했던 sample.txt가 존재하는지 확인해주세요.

누구나 쉽게 이해할 수 있는 Git 명령어

----

## [복제한 저장소에서 다시 푸시하기](https://backlog.com/git-tutorial/kr/intro/intro4_4.html)

이번에는 복제한 로컬 저장소에서 다시 원격 저장소로 파일을 푸시(push) 해 봅시다.

### 콘솔

tutorial2에서의 작업
우선 이전 페이지에서 복제한 저장소의 폴더에 있는 sample.txt파일을 열어 아래 굵은글자 부분의 내용을 추가하고 커밋합니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add 변경사항을 인덱스에 등록하기
```

```bash
$ git add sample.txt
$ git commit -m "add 설명을 추가함"
[master 1ef5c8c] add 설명을 추가함
 1 files changed, 1 insertions(+), 1 deletions(-)
```

tutorial2에서의 작업
이제 이 변경내역을 push 하여 원격 저장소를 업데이트합니다.

복제한 저장소에서 push 할 때는 파라미터 origin master를 생략할 수 있습니다.

```bash
$ git push
Username: <사용자명>
Password: <비밀번호>
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 351 bytes, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://monkey.backlogtool.com/git/BLG/tutorial.git
   486789c..1ef5c8c  master -> master
```

Backlog의 Git 페이지를 열어주십시오. 최근 변경내역에 방금 push 한 커밋이 추가되어 있을 겁니다.

![최근 업데이트에 지금 push 한 커밋이 추가](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro4_4_6.png)

----

## [원격 저장소에서 풀(Pull)해오기](https://backlog.com/git-tutorial/kr/intro/intro4_5.html)

원격 저장소에서 「tutorial」로 최신 변경 내용을 가져와 봅시다.

### 콘솔

이전 페이지에서 「tutorial2」로부터 원격 저장소로 보낸(Push) 내용을 내PC의「tutorial」폴더로 가져와(Pull) 봅시다.

풀을 수행하려면 pull 명령어를 사용합니다. 만약 저장소명이 생략되면 origin의 이름으로 등록되어 있는 저장소 밑에 pull을 수행하게 됩니다.

```bash
$ git pull <repository> <refspec>...
```

> tutorial에서의 작업

다음 명령어를 실행하십시오.

```bash
$ git pull origin master
Username: <사용자명>
Password: <비밀번호>
From https://monkey.backlogtool.com/git/BLG/tutorial
 * branch            master     -> FETCH_HEAD
Updating ac56e47..3da09c1
Fast-forward
 sample.txt |    1
 1 files changed, 1 insertions(+), 0 deletions(-)
```

sample.txt 파일의 내용이 업데이트되었습니다.

> tutorial에서의 작업

log 명령어로 이력을 확인 해 봅시다.

```bash
$ git log
commit 3da09c1134a41f2bee854a413916e4ebcae7318d
Author: eguchi <eguchi@nulab.co.jp>
Date:   Thu Jul 12 18:02:45 2012 +0900

    add 설명을 추가함

commit ac56e474afbbe1eab9ebce5b3ab48ac4c73ad60e
Author: eguchi <eguchi@nulab.co.jp>
Date:   Thu Jul 12 18:00:21 2012 +0900

    first commit
```

「tutorial2」에서 변경 한 이력의「add 설명 추가함」가 추가 되었습니다.

> tutorial에서의 작업

sample.txt 파일을 열고 내용을 확인해봅시다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add 변경사항을 인덱스에 등록하기
```

「add 변경사항을 인덱스에 등록하기」가 추가되어 있습니다.

----

# 변경 이력의 통합

## [변경 이력 병합(Merge)하기](https://backlog.com/git-tutorial/kr/intro/intro5_1.html)

### merge

![병합 예1](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro5_1_1.png)

내가 끌어온 저장소가 최신 버전이 아닌 경우, 즉 내가 pull 을 실행한 후 다른 사람이 push 를 하여 원격 저장소를 업데이트 해버린 경우에는 위의 그림과 같이 내 push 요청이 거부되어 버립니다.

![マージ 例2](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro5_1_2.png)

이런 경우 병합(merge)이라는 작업을 진행하여 다른 사람의 업데이트 이력을 내 저장소에도 갱신 해야합니다. 만약 병합하지 않은 채로 이력을 덮어쓰게 되면 다른 사람이 push 한 업데이트 내역(그림의 커밋C)이 사라져 버리기 때문입니다.

병합 기능을 이용하면 Git 이 현재 브랜치에 알아서 변경 사항을 통합해 준다고! 앗, 자동으로 통합이 될 수 없는 경우도 있지 않냐구? 다음 페이지에서 수동으로 하는 방법도 설명해 줄께!

----

## [충돌 해결하기](https://backlog.com/git-tutorial/kr/intro/intro5_2.html)

이전 페이지에서 설명한 것처럼, 병합 기능은 Git 에서 변경한 부분을 자동으로 통합해 주는 기능입니다. 그러나 경우에 따라 자동으로 병합할 수 없는 경우도 있습니다.

바로 원격 저장소와 로컬 저장소 양쪽에서 파일의 동일한 부분을 변경한 경우입니다. 이 경우 두 변경 내용중 어느 쪽을 저장할 것인지 자동으로 판단 할 수 없기 때문에 충돌이 발생합니다.

Git 은 충돌이 발생한 파일 내용을 아래 그림처럼 표시합니다. 이 부분을 우리가 직접 수정해 주어야 합니다.

![충돌 발생의 예](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro5_1_3.png)

===== 로 구분된 윗 부분이 로컬 저장소,
아랫 부분이 원격 저장소의 변경 내용이라는 점!

다음 그림과 같이 모든 충돌 부분을 수정한 후에, 다시 커밋을 수행하면 됩니다.

![競合の解決の例](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro5_1_4.png)

----

# 튜토리얼3 변경 이력의 통합

## [충돌상태 만들기](https://backlog.com/git-tutorial/kr/intro/intro6_1.html)

우선은 「tutorial」과 「tutorial2」를 사용하여 충돌 상태를 만들어봅시다.

### 콘솔

> tutorial에서의 작업

우선은 tutorial 폴더의 sample.txt를 열고, 다음과 같은 내용으로 수정하고 나서 커밋하십시오.

```txt
원숭이도 이해할 수 있는 Git 명령어
add 변경사항을 인덱스에 등록하기
commit 인덱스의 상태를 기록하기
```

```bash
$ git add sample.txt
$ git commit -m "commit의 설명 추가"
[master 95f15c9] commit의 설명 추가
 1 files changed, 1 insertions(+), 0 deletions(-)
```

tutorial2에서의 작업
그 다음, tutorial2 폴더의 sample.txt를 열고 이번엔 조금 다르게 아래 내용으로 수정하고 나서 커밋하십시오.

```txt
원숭이도 이해할 수 있는 Git 명령어
add 변경사항을 인덱스에 등록하기
pull 원격 저장소의 내용을 가져오기
```

```bash
$ git add sample.txt
$ git commit -m "pull 설명을 추가"
[master 4c01823] pull 설명을 추가
 1 files changed, 1 insertions(+), 0 deletions(-)
```

tutorial2에서의 작업
그 상태로 tutorial2에서 원격 저장소로 push합시다.

```bash
$ git push
Username: <사용자명>
Password: <비밀번호>
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 391 bytes, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://monkey.backlogtool.com/git/BLG/tutorial.git
   3da09c1..4c01823  master -> master
```

지금 원격 저장소 sample.txt파일 메시지 세 번째 행엔 "pull 원격 저장소의 내용을 취득함"이란 변경 이력이 기록되어 있다고!

> tutorial에서의 작업

이번에는 tutorial에서 원격 저장소로 push합시다.

```bash
$ git push
Username: <사용자명>
Password: <비밀번호>
To https://monkey.backlogtool.com/git/BLG/tutorial.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://monkey.backlogtool.com/git/BLG/tutorial.git'
To prevent you from losing history, non-fast-forward updates were rejected
Merge the remote changes (e.g. 'git pull') before pushing again.  See the
'Note about fast-forwards' section of 'git push --help' for details.
```

오류가 발생하여 push 를 거부(rejected)당했습니다.

----

## [충돌 해결하기](https://backlog.com/git-tutorial/kr/intro/intro6_2.html)

먼저 pull 을 실행하여, 원격 저장소의 최신 변경 이력을 로컬로 가져와 봅시다.

### 콘솔

> tutorial에서의 작업

다음 명령어를 실행하십시오.

```bash
$ git pull origin master
Username: <사용자 이름>
Password: <비밀번호>
remote: Counting objects: 5, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (3/3), done.
From https://monkey.backlogtool.com/git/BLG/tutorial
 * branch            master     -> FETCH_HEAD
Auto-merging sample.txt
CONFLICT (content): Merge conflict in sample.txt
Automatic merge failed; fix conflicts and then commit the result.
```

Merge 하던 중에 충돌이 발생했다는 것을 나타내는 메시지가 표시되었습니다.

> tutorial에서의 작업

「Merge conflict in sample.txt」라고 표시되어 있으므로 sample.txt 파일을 열어서 확인해봅니다.
Git이 자동으로 병합되지 않은 부분을 다음과 같이 변경했습니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add 변경 사항을 인덱스에 등록하기
<<<<<<< HEAD
commit 인덱스의 상태를 기록하기
=======
pull 원격 저장소의 내용을 가져오기
>>>>>>> 4c0182374230cd6eaa93b30049ef2386264fe12a
```

> tutorial에서의 작업


![수정하세요](https://backlog.com/git-tutorial/kr/img/post/img_modified_mascot.png)

여기에서는 양쪽 변경사항을 둘다 넣기로 하고, 불필요한 행은 삭제합니다

```txt
원숭이도 이해할 수 있는 Git 명령어
add 변경 사항을 인덱스에 등록하기
commit 인덱스의 상태를 기록하기
pull 원격 저장소의 내용을 가져오기
```

> tutorial에서의 작업

파일 내용에 변경사항이 생겼으니 다시 커밋해야겠죠.

```bash
$ git add sample.txt
$ git commit -m "병합"
[master d845b81] 병합
```

이로써 원격 저장소에서 최신 변경 내용 가져오기가 완료되었습니다.

> tutorial에서의 작업

log 명령어로 이력을 확인 해 봅시다. 'graph' 를 지정하면 선으로 된 그림 형태로 이력 흐름이 표시됩니다. 'oneline'을 선택하면 한 줄로 커밋 정보가 표시됩니다.

```bash
$ git log --graph --oneline
*   d845b81 병합
|\
| * 4c01823 pull 설명을 추가
* | 95f15c9 commit의 설명 추가
|/
* 3da09c1 add 설명을 추가
* ac56e47 first commit
```

이 표시로 두 가지 변경 사항이 통합됐음을 알 수 있습니다.

이로써 이전 페이지에서는 거부되었던 push 를 할 수 있게 되었습니다. push 해봅시다.

야호! 이걸로 Git의 기본적인 사용법에 대한 설명은 끝! 브랜치나 커밋 수정 같은 더 심도있는 내용을 알고 싶은 분은 발전 편에서 만나요!

----

# 브랜치 (Branch)
## [시작하기](https://backlog.com/git-tutorial/kr/intro/intro1_1.html)

안녕, 하카타에서 태어난 원숭이 킥킥이야. 오늘은 나랑 같이 버전 관리 시스템, 'Git(깃)' 을 공부해보자.

여러분은 파일을 편집 전 상태로 되돌리고 싶을 때 어떻게 하고 있나요?

가장 간단한 방법은 편집하기 전에 파일을 미리 복사해두는 것입니다. 파일과 폴더명 뒤에 편집한 날짜를 붙여주는 방식이죠. 하지만 파일을 편집할 때마다 매번 복사하는 일은 번거롭기도 하고 실수할 가능성도 많습니다.

![파일 백업의 예](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_1_1.png)

또한 위의 그림처럼 특별한 규칙 없이 마음대로 이름을 붙여놓는 경우 어느 파일이 최신인지, 또 파일의 어떤 부분이 변경된 것인지 파악하기 어렵습니다.

아래 그림을 보세요. 이렇게 여러 명이 공유한 파일을 동시에 편집하는 바람에 다른 사람이 먼저 변경하고 있던 내용을 지워버린 경험은 없나요?

![팀 작업의 실패 사례](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_1_2.png)

바로 이런 문제를 해결하기 위해 만들어진 것이 Git과 같은 버전 관리 시스템입니다.

### Git을 이용하여 버전 관리하기

Git이란 소스코드를 효과적으로 관리하기 위해 개발된 '분산형 버전 관리 시스템'입니다. 원래는 Linux 소스코드를 관리할 목적으로 개발 되었습니다.

Git에서는 소스 코드가 변경된 이력을 쉽게 확인할 수 있고, 특정 시점에 저장된 버전과 비교하거나 특정 시점으로 되돌아갈 수도 있습니다.

또 내가 올리려는 파일이 누군가 편집한 내용과 충돌한다면, 서버에 업로드 할 때 경고 메시지가 발생됩니다. 누군가가 애써 편집한 내용을 덮어써버리는 실수는 이제 없겠죠!

![팀 작업에 버전관리 활용하기](https://backlog.com/git-tutorial/kr/img/post/intro/capture_intro1_1_3.png)

Git으로 파일을 관리하면, 업데이트 이력이 Git에 저장되지.

매번 백업용 파일 복사본을 만들 필요가 없으니까 엄청 편하고 깔끔하다구!

---

## [브랜치란?](https://backlog.com/git-tutorial/kr/stepup/stepup1_1.html)

지금까지 Git의 기본적인 사용법에 대해 알아 보았습니다. 발전 편에서는 브랜치의 사용법에 대해 좀 더 자세히 알아보도록 하겠습니다.

소프트웨어를 개발할 때에 개발자들은 동일한 소스코드를 함께 공유하고 다루게 됩니다. 동일한 소스코드 위에서 어떤 개발자는 버그를 수정하기도 하고 또 다른 개발자는 새로운 기능을 만들어 내기도 하죠. 이와 같이 여러 사람이 동일한 소스코드를 기반으로 서로 다른 작업을 할 때에는 각각 서로 다른 버전의 코드가 만들어 질 수 밖에 없습니다.

이럴 때, 여러 개발자들이 동시에 다양한 작업을 할 수 있게 만들어 주는 기능이 바로 '브랜치(Branch)' 입니다. 각자 독립적인 작업 영역(저장소) 안에서 마음대로 소스코드를 변경할 수 있지요. 이렇게 분리된 작업 영역에서 변경된 내용은 나중에 원래의 버전과 비교해서 하나의 새로운 버전으로 만들어 낼 수 있습니다.

### 브랜치(branch)란?

브랜치란 독립적으로 어떤 작업을 진행하기 위한 개념입니다. 필요에 의해 만들어지는 각각의 브랜치는 다른 브랜치의 영향을 받지 않기 때문에, 여러 작업을 동시에 진행할 수 있습니다.

![ブランチとは](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_1_1.png)

또한 이렇게 만들어진 브랜치는 다른 브랜치와 병합(Merge)함으로써, 작업한 내용을 다시 새로운 하나의 브랜치로 모을 수 있습니다.

아래 그림을 보면, 브랜치를 사용하여 동시에 여러 작업을 진행할 때의 작업 흐름을 한눈에 파악할 수 있습니다.

여러 명이서 동시에 작업을 할 때에 다른 사람의 작업에 영향을 주거나 받지 않도록, 먼저 메인 브랜치에서 자신의 작업 전용 브랜치를 만듭니다. 그리고 각자 작업을 진행한 후, 작업이 끝난 사람은 메인 브랜치에 자신의 브랜치의 변경 사항을 적용합니다. 이렇게 함으로써 다른 사람의 작업에 영향을 받지 않고 독립적으로 특정 작업을 수행하고 그 결과를 하나로 모아 나가게 됩니다. 이러한 방식으로 작업할 경우 '작업 단위', 즉 브랜치로 그 작업의 기록을 중간 중간에 남기게 되므로 문제가 발생했을 경우 원인이 되는 작업을 찾아내거나 그에 따른 대책을 세우기 쉬워집니다.

![브랜치를 사용한 병행 작업](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_1_2.png)

### master 브랜치

저장소를 처음 만들면, Git은 바로 'master'라는 이름의 브랜치를 만들어 둡니다. 이 새로운 저장소에 새로운 파일을 추가 한다거나 추가한 파일의 내용을 변경하여 그 내용을 저장(커밋, Commit)하는 것은 모두 'master' 라는 이름의 브랜치를 통해 처리할 수 있는 일이 됩니다.

'master'가 아닌 또 다른 새로운 브랜치를 만들어서 '이제부터 이 브랜치를 사용할거야!'라고 선언(체크아웃, checkout)하지 않는 이상, 이 때의 모든 작업은 'master' 브랜치에서 이루어 집니다.

![masterブランチ](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_1_3.png)

----

## [브랜치 만들기](https://backlog.com/git-tutorial/kr/stepup/stepup1_2.html)

Git 에서는 작업에 따라 자유롭게 브랜치를 만들 수 있습니다. 그러나 이것을 효과적으로 관리하려면, 먼저 함께 작업할 팀원들과 어떠한 방식으로 브랜치를 만들고 통합할 것인지 미리 정해두는 것이 좋습니다. 예를 들어 새로운 브랜치를 만들 때에 브랜치 이름은 어떤 규칙으로 지을 것인지 또는 어떤 상황에서 브랜치를 만들 지, 어느 시점에 통합할 것인지 등등 규칙은 정하기 나름입니다.

자, 그럼 이제부터 우리가 만들 수 있는 브랜치에는 어떤 종류가 있는지 살펴 보도록 하겠습니다.

### 통합 브랜치(Integration Branch)

통합 브랜치란 언제든지 배포할 수 있는 버전을 만들 수 있어야 하는 브랜치 입니다. 그렇기 때문에 늘 안정적인 상태를 유지하는 것이 중요합니다. 여기서 '안정적인 상태'란 현재 작업 중인 소스코드가 모바일에서 동작하는 어플리케이션을 개발하기 위한 것이라면, '그 어플리케이션의 모든 기능이 정상적으로 동작하는 상태'를 의미합니다.

만약 이 어플리케이션에 어떤 문제가 발견되어 그 문제(버그)를 수정한다던지 새로운 기능을 추가해야 한다던지 해야할 때, 바로 '토픽 브랜치(Topic branch)'를 만들 수 있습니다. 처음에는 보통 통합 브랜치에서 토픽 브랜치를 만들어 냅니다.

일반적으로 저장소를 처음 만들었을 때에 생기는 'master' 브랜치를 통합 브랜치로 사용합니다.

### 토픽 브랜치(Topic Branch)

토픽 브랜치란, 기능 추가나 버그 수정과 같은 단위 작업을 위한 브랜치 입니다. 여러 개의 작업을 동시에 진행할 때에는, 그 수만큼 토픽 브랜치를 생성할 수 있습니다.

토픽 브랜치는 보통 통합 브랜치로부터 만들어 내며, 토픽 브랜치에서 특정 작업이 완료되면 다시 통합 브랜치에 병합하는 방식으로 진행됩니다. 이러한 토픽 브랜치는 '피처 브랜치(Feature branch)' 라고 부르기도 합니다.

![토픽 브랜치 이미지](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_2_1.png)

----

## [브랜치 전환하기](https://backlog.com/git-tutorial/kr/stepup/stepup1_3.html)

Git 에서는 항상 작업할 브랜치를 미리 선택해야 합니다. 처음에 Git을 설치하게 되면 'master' 브랜치가 선택되어 있죠. 현재 선택된 브랜치가 아닌 다른 브랜치에서 작업하고 싶을 때에는, '체크아웃(checkout)' 명령어를 실행하여 원하는 브랜치로 전환할 수 있습니다. 체크아웃을 실행하면, 우선 브랜치 안에 있는 마지막 커밋 내용이 작업 트리에 펼쳐집니다. 브랜치가 전환 되었으므로 이 후에 실행한 커밋은 전환한 브랜치에 추가됩니다.

![ブランチの切り替え](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_3_1.png)

### HEAD

'HEAD' 란 현재 사용 중인 브랜치의 선두 부분을 나타내는 이름입니다. 기본적으로는 'master'의 선두 부분을 나타냅니다. 'HEAD' 를 이동하면, 사용하는 브랜치가 변경됩니다.

Note

커밋을 지정할 때, '~(틸드, 물결기호)'와 '^(캐럿, 삽입기호)'을 사용하여 현재 커밋으로부터 특정 커밋의 위치를 가리킬 수 있습니다. 이 때 자주 사용하는 것이 'HEAD' 로서, '~(틸드)'와 숫자를 'HEAD' 뒤에 붙여 몇 세대 앞의 커밋을 가리킬 수 있습니다. '^(캐럿)'은, 브랜치 병합에서 원본이 여럿 있는 경우 몇 번째 원본인지를 지정할 수 있습니다.

![틸드(물결기호)와 캐럿(삽입기호)을 이용 중인 커밋으로부터의 상대적인 위치 지정](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_3_2.png)

### stash

커밋하지 않은 변경 내용이나 새롭게 추가한 파일이 인덱스와 작업 트리에 남아 있는 채로 다른 브랜치로 전환(checkout)하면, 그 변경 내용은 기존 브랜치가 아닌 전환된 브랜치에서 커밋할 수 있습니다.

단, 커밋 가능한 변경 내용 중에 전환된 브랜치에서도 한 차례 변경이 되어 있는 경우에는 체크아웃에 실패할 수 있습니다. 이 경우 이전 브랜치에서 커밋하지 않은 변경 내용을 커밋하거나, stash 를 이용해 일시적으로 변경 내용을 다른 곳에 저장하여 충돌을 피하게 한 뒤 체크아웃을 해야 합니다.

stash 란, 파일의 변경 내용을 일시적으로 기록해두는 영역입니다. stash 를 사용하여 작업 트리와 인덱스 내에서 아직 커밋하지 않은 변경을 일시적으로 저장해 둘 수 있습니다. 이 stash 에 저장된 변경 내용은 나중에 다시 불러와 원래의 브랜치나 다른 브랜치에 커밋할 수 있습니다.

![stash](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_3_3.png)

----

## [브랜치 통합하기](https://backlog.com/git-tutorial/kr/stepup/stepup1_4.html)

작업이 완료된 토픽 브랜치는 최종적으로 통합 브랜치에 병합됩니다. 브랜치 통합에는merge 를 사용하는 방법과 'rebase'를 사용하는 방법의 2가지 종류가 있습니다. 어느 쪽을 사용하느냐에 따라 통합 후의 브랜치의 이력이 크게 달라집니다.

### merge

merge 를 사용하면, 여러 개의 브랜치를 하나로 모을 수 있습니다.

예를 들어, 아래 그림과 같이 'master' 브랜치에서 분기하는 'bugfix'라는 브랜치가 있다고 가정해 봅시다.

![브랜치](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_4_1.png)

이 'bugfix' 브랜치를 'master' 브랜치로 병합할 때, 'master' 브랜치의 상태가 이전부터 변경되어 있지만 않으면 매우 쉽게 병합할 수 있습니다. 'bugfix' 브랜치의 이력은 'master' 브랜치의 이력을 모두 포함하고 있기 때문에, 'master' 브랜치는 단순히 이동하기만 해도 'bugfix' 브랜치의 내용을 적용할 수 있습니다. 또한 이 같은 병합은 'fast-forward(빨리 감기) 병합'이라고 부릅니다.

![fast-forward(빨리감기) 병합](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_4_2.png)

하지만 'bugfix' 브랜치를 분기한 이후에 'master' 브랜치에 여러 가지 변경 사항이 적용되는 경우도 있습니다. 이 경우에는 'master' 브랜치 내의 변경 내용과 'bugfix' 브랜치 내의 변경 내용을 하나로 통합할 필요가 있습니다.

![브랜치 분기 후 'master'에 변경 사항이 생긴 경우](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_4_3.png)

따라서 양쪽의 변경을 가져온 'merge commit(병합 커밋)'을 실행하게 됩니다. 병합 완료 후, 통합 브랜치인 'master' 브랜치로 통합된 이력이 아래 그림과 같이 생기게 됩니다.

![양쪽의 변경을 적용한 'merge commit(병합 커밋)'](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_4_4.png)

Note

병합 실행 시에 'fast-forward 병합'이 가능한 경우라도 'non fast-forward 병합' 옵션을 지정하여 아래 그림과 같이 만들어 낼 수도 있습니다.

![non fast-forward 병합](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_4_5.png)

'non fast-forward 병합'을 실행하면, 브랜치가 그대로 남기 때문에 그 브랜치로 실행한 작업 확인 및 브랜치 관리 면에서 더 유용할 수 있습니다.

### rebase

위와 마찬가지로, 'master' 브랜치에서 분기하는 'bugfix' 브랜치가 있다고 가정합니다.

![브랜치](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_4_6.png)

이제 rebase 를 이용해 어떻게 브랜치를 통합할 수 있는지 알아볼 차례 입니다. 아래 그림과 같이 'non fast-forward 병합' 방식으로 진행되는 시나리오를 만들어 봅시다.

![rebase를 사용하여 브랜치 통합](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_4_7.png)

우선 'bugfix' 브랜치를 'master' 브랜치에 rebase 하면, 'bugfix' 브랜치의 이력이 'master' 브랜치 뒤로 이동하게 됩니다. 그 때문에 그림과 같이 이력이 하나의 줄기로 이어지게 됩니다.

이 때 이동하는 커밋 X와 Y 내에 포함되는 내용이 'master'의 커밋된 버전들과 충돌하는 부분이 생길 수 있습니다. 그 때는 각각의 커밋에서 발생한 충돌 내용을 수정할 필요가 있습니다.

![rebase를 사용하여 브랜치 통합](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_4_8.png)

'rebase'만 하면 아래 그림에서와 같이, 'master'의 위치는 그대로 유지됩니다. 'master' 브랜치의 위치를 변경하기 위해서는 'master' 브랜치에서 'bugfix' 브랜치를 fast-foward(빨리감기) 병합 하면 됩니다.

![rebase를 사용하여 브랜치 통합](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_4_9.png)

Note

merge 와 rebase 는 통합 브랜치에 토픽 브랜치를 통합하고자 하는 목적은 같으나, 그 특징은 약간 다릅니다.

- merge
    변경 내용의 이력이 모두 그대로 남아 있기 때문에 이력이 복잡해짐.
- rebase
    이력은 단순해지지만, 원래의 커밋 이력이 변경됨. 정확한 이력을 남겨야 할 필요가 있을 경우에는 사용하면 안됨.

merge 와 rebase 는 팀 운용 방침에 따라 구별해 쓸 수 있습니다.
예를 들어 이력을 하나로 모두 모아서 처리하도록 운용한다고 치면 아래와 같이 구별해 사용할 수 있습니다.

- 토픽 브랜치에 통합 브랜치의 최신 코드를 적용할 경우에는 rebase 를 사용,
- 통합 브랜치에 토픽 브랜치를 불러올 경우에는 우선 rebase 를 한 후 merge

----

## [토픽 브랜치와 통합 브랜치에서의 작업 흐름 파악하기](https://backlog.com/git-tutorial/kr/stepup/stepup1_4.html)

토픽 브랜치와 통합 브랜치를 사용한 작업은 어떠한 순서로 진행되는 지, 간단한 예를 통해 알아보도록 하겠습니다.

다음과 같이 토픽 브랜치에서 새로운 기능을 추가하는 작업과 버그 수정 작업을 동시에 진행 하는 경우를 생각해 봅시다.

![기능을 추가하는 토픽 브랜치에서 작업을 실행하는 도중에, 버그 수정을 해야 하는 상황이 됐다](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_5_1.png)

일단 통합 브랜치로부터 새롭게 버그 수정용 토픽 브랜치를 만들어, 새로운 기능을 추가하는 작업과는 별개로 버그 수정 작업을 진행할 수 있습니다.

![새로 버그 수정용 토픽 브랜치를 만들어, 기능 추가와는 독립된 상태로 작업을 시작할 수 있음](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_5_2.png)

버그 수정을 완료한 후, 통합 브랜치와 버그 수정용 토픽 브랜치를 병합하여 수정된 버전을 만들어 낼 수 있습니다.

![원래의 통합 브랜치에 적용하여 보완된 버전을 만들어 낼 수 있음](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_5_3.png)

버그도 수정 했으니, 다시 원래 브랜치로 돌아와서 새로운 기능 추가 작업을 계속 진행하려 합니다.

![원래 브랜치로 돌아와서 기능 추가 작업을 계속 수행할 수 있다](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_5_4.png)

그러나, 작업을 진행하려고 봤더니 앞서 적용한 커밋 X 의 버그가 수정된 버전의 소스코드를 지금의 커밋 O 에도 적용해야만 한다는 사실을 알게 되었습니다. 여기서 커밋 X 의 내용을 적용하려면, 직접 merge 하는 방법과 커밋 X 를 적용한 통합 브랜치에 rebase 하는 방법이 있습니다.

여기서는 통합 브랜치에 rebase 하는 방법을 이용해 보겠습니다.

![통합 브랜치에 rebase](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_5_5.png)

이런 상황에서는, rebase 를 이용하여 커밋 X 의 내용을 적용한 상태로 새로운 기능을 추가하기 위해 아래 그림과 같이 O' 버전으로 만들어 내는 방법을 이용하면 됩니다.

브랜치를 능숙하게 잘~ 사용하면 상황에 맞게 여러 작업을 동시에 진행할 수 있다구!

## 컬럼 「A successful Git branching model」- 성공적인 Git 브랜칭 모델

Git의 브랜치 운용 모델로서, "A successful Git branching model" 이란 컬럼을 소개합니다.

원문:
[http://nvie.com/posts/a-successful-git-branching-model/](http://nvie.com/posts/a-successful-git-branching-model/)

이 운용 모델에서는 크게 나눠 4가지 종류의 브랜치를 이용하여 개발을 진행합니다.

- 메인 브랜치(Main branch)
- 피처 브랜치(Feature branch) 또는 토픽 브랜치(Topic branch)
- 릴리스 브랜치(Release branch)
- 핫픽스 브랜치(Hotfix branch)

![Git의 브랜치 운용 모델](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup1_5_6.png)

### 메인 브랜치(Main branch)

'master' 브랜치와 'develop' 브랜치, 이 두 종류의 브랜치를 보통 메인 브랜치로 사용합니다.

- master
    'master' 브랜치에서는, 배포 가능한 상태만을 관리합니다. 커밋할 때에는 태그를 사용하여 배포 번호를 기록합니다.
- develop
    'develop' 브랜치는 앞서 설명한 통합 브랜치의 역할을 하며, 평소에는 이 브랜치를 기반으로 개발을 진행합니다.

### 피처 브랜치(Feature branch)

피처 브랜치는, 앞서 설명한 토픽 브랜치 역할을 담당합니다.

이 브랜치는 새로운 기능 개발 및 버그 수정이 필요할 때에 'develop' 브랜치로부터 분기합니다. 피처 브랜치에서의 작업은 기본적으로 공유할 필요가 없기 때문에, 원격으로는 관리하지 않습니다. 개발이 완료되면 'develop' 브랜치로 병합하여 다른 사람들과 공유합니다.

### 릴리즈 브랜치(Release branch)

릴리즈 브랜치에서는 버그를 수정하거나 새로운 기능을 포함한 상태로 모든 기능이 정상적으로 동작하는지 확인합니다. 릴리즈 브랜치의 이름은 관례적으로 브랜치 이름 앞에 'release-' 를 붙입니다. 이 때, 다음 번 릴리즈를 위한 개발 작업은 'develop' 브랜치 에서 계속 진행해 나가면 됩니다.

릴리즈 브랜치에서는 릴리즈를 위한 최종적인 버그 수정 등의 개발을 수행합니다. 모든 준비를 마치고 배포 가능한 상태가 되면 'master' 브랜치로 병합시키고, 병합한 커밋에 릴리즈 번호 태그를 추가합니다.

릴리즈 브랜치에서 기능을 점검하며 발견한 버그 수정 사항은 'develop' 브랜치에도 적용해 주어야 합니다. 그러므로 배포 완료 후 'develop' 브랜치에 대해서도 병합 작업을 수행합니다.

### 핫픽스 브랜치(Hotfix branch)

배포한 버전에 긴급하게 수정을 해야 할 필요가 있을 경우, 'master' 브랜치에서 분기하는 브랜치입니다. 관례적으로 브랜치 이름 앞에 'hotfix-'를 붙입니다.

예를 들어 'develop' 브랜치에서 개발을 한창 진행하고 있는 도중에 이전에 배포한 소스코드에 아주 큰 버그가 발견되는 경우를 생각해 보세요. 문제가 되는 부분을 빠르게 수정해서 안정적으로 다시 배포해야 하는 상황입니다. 'develop' 브랜치에서 문제가 되는 부분을 수정하여 배포 가능한 버전을 만들기에는 시간도 많이 소요되고 안정성을 보장하기도 어렵습니다. 그렇기 때문에 바로 배포가 가능한 'master' 브랜치에서 직접 브랜치를 만들어 필요한 부분 만을 수정한 후 다시 'master'브랜치에 병합하여 이를 배포하려고 하는 것이죠.

이 때 만든 핫픽스 브랜치에서의 변경 사항은 'develop' 브랜치에도 병합하여 문제가 되는 부분을 처리해 주어야 합니다.

----

# 튜토리얼1: 브랜치를 사용해보자

## [0. 사전 준비](https://backlog.com/git-tutorial/kr/stepup/stepup2_1.html)

실습을 위해 먼저 Git 저장소를 만들어야 합니다.

아래 코드를 이용하여 tutorial 이라는 이름으로 새 폴더를 만들고 Git 저장소로 지정해 봅시다.

```bash
$ mkdir tutorial
$ cd tutorial
$ git init
Initialized empty Git repository in /Users/eguchi/Desktop/tutorial/.git/
```

tutorial 폴더에 myfile.txt 이라는 이름으로 파일을 만든 후 커밋합니다.

```txt
원숭이도 이해할 수 있는 Git 명령어

$ git add myfile.txt
$ git commit -m "first commit"
[master (root-commit) a73ae49] first commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 myfile.txt
```

여기까지 진행했다면, 아래 그림과 같은 이력이 남게 됩니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_1_1.png)

----

## [1. 브랜치 만들기](https://backlog.com/git-tutorial/kr/stepup/stepup2_2.html)

'issue1' 이라는 이름으로 새로운 브랜치를 작성합니다.

브랜치는 branch 란 명령어로 만들 수 있습니다.

```bash
$ git branch <branchname>
```

'issue1' 이라는 이름으로 브랜치를 만들어 봅시다.

```bash
$ git branch issue1
```

옵션을 지정하지 않고 branch 명령어를 실행하면 브랜치 목록 전체를 확인할 수 있습니다. 앞 부분에 * 이 붙어있는 것이 현재 선택된 브랜치입니다.

```bash
$ git branch
  issue1
* master
```

이 시점까지의 이력을 보면 다음과 같습니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_2_1.png)

----

## [2. 브랜치 전환하기](https://backlog.com/git-tutorial/kr/stepup/stepup2_3.html)

앞에서 우리가 새로 만든 'issue1'라는 이름의 브랜치를 사용하여 어떤 작업을 수행하려면, 이 브랜치를 사용 하겠다고 명시적으로 지정해 주어야 합니다. 이 때 사용하는 명령어가 바로 checkout 입니다. 체크아웃(checkout)이란, 내가 사용할 브랜치를 지정하는 것을 의미합니다.

다음과 같이checkout 명령어 뒤에 사용할 브랜치 이름을 입력하면 됩니다.

```bash
$ git checkout <branch>
```

아래와 같이 입력하여 'issue1' 브랜치를 체크아웃 해 봅시다.

```bash
$ git checkout issue1
Switched to branch 'issue1'
```

이 시점까지의 이력을 보면 아래와 같습니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_3_1.png)

Note

checkout 명령에 -b 옵션을 넣으면 브랜치 작성과 체크아웃을 한꺼번에 실행할 수 있습니다.

```bash
$ git checkout -b <branch>
```

'issue1' 브랜치를 체크아웃한 상태에서 커밋을 수행하면, 'issue1' 브랜치에 그 이력이 기록됩니다. mylife.txt 에 아래 박스에서와 같이 문장을 추가한 후에 커밋해봅시다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기

$ git add myfile.txt
$ git commit -m "add 설명을 추가"
[issue1 b2b23c4] add 설명을 추가
 1 files changed, 1 insertions(+), 0 deletions(-)
```

위와 같이 commit 명령어에 -m 옵션을 넣으면 커밋 설명을 포함시킬 수 있습니다.

이 시점까지의 이력을 보면 다음과 같습니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_3_2.png)

----

## [3. 브랜치 병합하기](https://backlog.com/git-tutorial/kr/stepup/stepup2_4.html)

이번에는 'issue1' 브랜치의 변경 사항을 'master' 브랜치에 병합해 볼까요?

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_3_2.png)

브랜치 병합은 merge 명령어로 실행합니다. 이 명령어에 병합할 커밋 이름을 넣어 실행하면, 지정한 커밋 내용이 'HEAD'가 가리키고 있는 브랜치에 넣어집니다. 'HEAD'는 현재 사용중인 브랜치에 위치하게 됩니다. 위 그림에서는 'issue1' 커밋에 'HEAD'가 위치하고 있습니다.

```bash
$ git merge <commit>
```

'master' 브랜치에 'issue1'를 넣기 위해서는 우선 'master' 브랜치에 'HEAD'가 위치하게 만들어야 합니다. 이 때에는 checkout 명령어를 이용하여 현재 사용중인 브랜치를 'master'로 전환합니다.

```bash
$ git checkout master
Switched to branch 'master'
```

병합하기 전에 myfile.txt 파일을 열어 내용을 확인합니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
```

이번 실습에서의 파일 편집은 'issue1' 브랜치에서 실행 했기 때문에 'master' 브랜치로 브랜치를 전환한 지금, myfile.txt 파일을 확인했을 때 그 내용이 변경되어 있지 않아야 합니다.

그럼 이제 병합을 시작해볼까요?

```bash
$ git merge issue1
Updating 1257027..b2b23c4
Fast-forward
 myfile.txt |    1
 1 files changed, 1 insertions(+), 0 deletions(-)
```

이제 'master' 브랜치가 가리키는 커밋이 'issue1'과 같은 위치로 이동했습니다. 이런 방식의 병합을 'fast-forward (빨리감기) 병합'이라고 합니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_4_1.png)

myfile.txt 파일을 열어 내용을 확인해 봅시다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
```

「add: 변경 사항을 만들어서 인덱스에 등록해보기」 내용이 추가되어 있는 것을 확인합니다.

----

## [4. 브랜치 삭제하기](https://backlog.com/git-tutorial/kr/stepup/stepup2_5.html)

'issue1' 브랜치의 내용이 모두 'master'에 통합 되었기 때문에 이제 더 이상 'issue1' 브랜치가 필요없게 되었습니다.

브랜치를 삭제하려면 branch 명령에 -d 옵션을 지정하여 실행하면 됩니다.

```bash
$ git branch -d <branchname>
```

'issue1' 브랜치를 삭제하려면, 다음 명령어를 실행합니다.

```bash
$ git branch -d issue1
Deleted branch issue1 (was b2b23c4).
```

이제 'issue1' 브랜치는 삭제되었습니다. 정말로 브랜치가 잘 삭제 되었는지 branch 명령어를 이용해서 확인합니다. 아래와 같이 'master' 브랜치만 목록에 남아 있게 됩니다.

```bash
$ git branch
* master
```

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_5_1.png)

----

## [5. 동시에 여러 작업하기](https://backlog.com/git-tutorial/kr/stepup/stepup2_6.html)

이번에는 두 개의 브랜치를 생성하여 동시에 여러 작업을 처리하는 상황을 만들어 보겠습니다.

'issue2' 와 'issue3' 브랜치를 만든 후, 'issue2' 브랜치로 전환 합니다.

```bash
$ git branch issue2
$ git branch issue3
$ git checkout issue2
Switched to branch 'issue2'
$ git branch
* issue2
  issue3
  master
```

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_6_1.png)

'issue2' 브랜치의 myfile.txt 에 아래와 같이 commit 에 대한 설명을 추가하여 커밋해 보도록 하겠습니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
commit: 인덱스 상태를 기록하기

$ git add myfile.txt
$ git commit -m "commit의 설명 추가"
[issue2 8f7aa27] commit의 설명 추가
 1 files changed, 2 insertions(+), 0 deletions(-)
```

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_6_2.png)

이번에는 'issue3' 브랜치로 전환 합니다.

```bash
$ git checkout issue3
Switched to branch 'issue3'
```

myfile.txt 파일을 열어 내용을 확인합니다. commit 명령의 설명은 'issue2' 브랜치에서 추가했기 때문에, 'issue3' 브랜치로 전환한 후의 myfile.txt 파일에는 add 명령의 설명 밖에 없습니다.

이번에는 pull 명령어의 설명을 추가하여 변경 사항을 커밋해 보도록 하겠습니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
pull: 원격 저장소의 내용을 가져오기

$ git add myfile.txt
$ git commit -m "pull 설명을 추가"
[issue3 e5f91ac] pull 설명을 추가
 1 files changed, 2 insertions(+), 0 deletions(-)
```

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_6_3.png)

지금까지 'issue2' 브랜치에 commit 에 대한 설명을, 'issue3' 브랜치에 pull 에 대한 설명을 포함하여 커밋해 보았습니다. 이처럼 각각의 브랜치에서는 독립적으로 서로 다른 작업을 처리할 수 있습니다.

다음 단계에서는 이 두 브랜치를 병합하여, 내용이 달라진 myfile.txt 파일에 대한 충돌을 해결하는 방법에 대해 알아보도록 하겠습니다.

----

## [6. 병합할 때 발생하는 충돌 해결하기](https://backlog.com/git-tutorial/kr/stepup/stepup2_7.html)

이번에는 'issue2' 브랜치에서 변경한 부분과 'issue3' 브랜치에서 변경한 부분을 모두 'master' 브랜치에 통합해 보도록 하겠습니다.

먼저 'master' 브랜치를 체크아웃한 다음 'issue2' 브랜치를 병합합니다.

```bash
$ git checkout master
Switched to branch 'master'
$ git merge issue2
Updating b2b23c4..8f7aa27
Fast-forward
 myfile.txt |    2 ++
 1 files changed, 2 insertions(+), 0 deletions(-)
```

이렇게 하면 앞서 설명되었던 'fast-forward(빨리감기) 병합'이 실행됩니다. 아래 그림을 보면, 'master' 브랜치에 'issue2' 브랜치가 병합된 것을 확인할 수 있습니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_7_1.png)

이번에는 'issue3' 브랜치를 병합합니다.

```bash
$ git merge issue3
Auto-merging myfile.txt
CONFLICT (content): Merge conflict in myfile.txt
Automatic merge failed; fix conflicts and then commit the result.
```

'CONFLICT(충돌)'이라 나오는 것을 보니 자동 병합에 실패한 것 같습니다. 앞서 각각의 브랜치에서 변경한 내용이 myfile.txt 의 같은 행에 포함되어 있기 때문입니다. 실제로 myfile.txt 의 내용을 확인해 보면 다음과 같이 변경되어 있습니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
<<<<<<< HEAD
commit: 인덱스의 상태를 기록하기
=======
pull: 원격 저장소의 내용을 가져오기
>>>>>>> issue3
```

![수정하세요](https://backlog.com/git-tutorial/kr/img/post/img_modified_mascot.png)

충돌이 있는 부분에 Git 이 자동으로 위와 같이 충돌 정보를 포함하여 파일 내용을 변경합니다. 이 내용을 통해 어떤 브랜치에서 어떤 부분이 충돌되었는지 확인할 수 있습니다. 충돌이 일어난 부분은 이렇게 일일이 확인해서 수정해 주어야 합니다. 그럼 아래와 같이 파일 내용을 변경해 봅시다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
commit: 인덱스의 상태를 기록하기
pull: 원격 저장소의 내용을 가져오기
```

충돌 부분을 모두 수정했으므로, 다시 커밋합니다.

```bash
$ git add myfile.txt
$ git commit -m "issue3 브랜치 병합"
## On branch master
nothing to commit (working directory clean)
```

이 시점까지의 이력을 보면 다음과 같습니다. 이번 병합은 충돌 부분을 수정했기 때문에 그 변화를 기록하는 병합 커밋이 새로 생성 되었습니다. 그리고 'master' 브랜치의 시작('HEAD')이 그 위치로 이동해 있는 것을 확인할 수 있습니다. 아래와 같은 방식을 'non fast-forward 병합'이라고 합니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_7_2.png)

----

## [7. rebase 로 병합하기](https://backlog.com/git-tutorial/kr/stepup/stepup2_8.html)

앞선 튜토리얼에서 우리는 두 개의 브랜치를 'master' 브랜치로 모두 병합 시켰습니다. 그로 인해 두 개의 줄기로 브랜치가 분기 되었다가 다시 하나로 합쳐지는 것을 확인 했었습니다.

'issue3' 브랜치를 병합 할 때에 rebase 를 먼저 실행한 후 병합을 시도한다면 그 이력을 하나의 줄기로 만들 수도 있습니다. 이번에는 이와 같은 경우를 만들어 보도록 하겠습니다. 이를 위해 일단 이전의 튜토리얼에서 마지막으로 진행했던 병합 명령을 취소합니다.

```bash
$ git reset --hard HEAD~
```

![rebase전의 기록 ](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_8_1_1.png)

이제 'issue3' 브랜치로 전환하여 'master' 브랜치에 rebase 를 실행합니다.

```bash
$ git checkout issue3
Switched to branch 'issue3'
$ git rebase master
First, rewinding head to replay your work on top of it...
Applying: pull 설명을 추가
Using index info to reconstruct a base tree...
<stdin>:13: new blank line at EOF.
+
warning: 1 line adds whitespace errors.
Falling back to patching base and 3-way merge...
Auto-merging myfile.txt
CONFLICT (content): Merge conflict in myfile.txt
Failed to merge in the changes.
Patch failed at 0001 pull 설명을 추가

When you have resolved this problem run "git rebase --continue".
If you would prefer to skip this patch, instead run "git rebase --skip".
To check out the original branch and stop rebasing run "git rebase --abort".
```

merge 때와 마찬가지로 myfile.txt 파일 내용에 충돌이 있기 때문에 그 부분을 이전의 튜토리얼에서와 동일하게 처리합니다. 충돌난 파일 내용을 적절히 변경해 주세요.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
<<<<<<< HEAD
commit: 인덱스의 상태를 기록하기
=======
pull: 원격 저장소의 내용을 가져오기
>>>>>>> issue3
```

rebase 의 경우 충돌 부분을 수정 한 후에는 commit 이 아니라 rebase 명령에 --continue 옵션을 지정하여 실행해야 합니다.

```bash
$ git add myfile.txt
$ git rebase --continue
```

Applying: pull 설명을 추가

만약 rebase 자체를 취소하려면 --abort 옵션을 지정하면 됩니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_8_1.png)

이전 튜토리얼에서 merge 명령어를 사용했을 때와 같이, rebase 만 실행한 경우에는 위의 그림처럼 'issue3' 브랜치가 두 브랜치의 앞 쪽으로 위치가 옮겨졌을 뿐 'master' 브랜치는 아직 'issue3'의 변경 사항이 적용되지 못한 상태로 뒤에 남겨져 있습니다. 이제 'master' 브랜치로 전환 하여 'issue3' 브랜치의 변경 사항을 모두 병합할 차례입니다.

```bash
$ git checkout master
Switched to branch 'master'
$ git merge issue3
Updating 8f7aa27..96a0ff0
Fast-forward
 myfile.txt |    1
 1 files changed, 1 insertions(+), 0 deletions(-)
```

myfile.txt 의 최종적인 내용은merge 했을 경우와 동일하지만, 그 이력은 아래 그림과 같이 달라집니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup2_8_2.png)

----

# 원격 저장소

## [pull, 원격 저장소의 데이터를 로컬 저장소에 가져와 병합하기](https://backlog.com/git-tutorial/kr/stepup/stepup3_1.html)

입문 편에서 설명한 바와 같이, pull 을 실행하면 원격 저장소의 변경된 데이터를 가져올 수 있습니다. 경우에 따라 로컬 저장소에 pull 한 데이터가 어떻게 반영 되는지 그림을 통해 확인해 보도록 하겠습니다.

먼저 아래 그림과 같이 로컬 저장소의 모든 변경 사항이 반영되어 있는 상태에서 새로운 변경 사항이 있는 원격 저장소의 커밋 Y 를 로컬로 가져오는 경우를 살펴 보도록 하겠습니다.

![로컬 브랜치에 변경 사항이 없는 경우](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup3_1_1.png)

이런 경우, 단순히 'fast-forward 병합'이 이루어집니다. 그림 속의 'master'는 로컬 저장소의 'master' 브랜치, 'origin/master'는 원격 저장소 'origin'의 'master' 브랜치를 나타냅니다.

![fast-forward 병합](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup3_1_2.png)

그러나 로컬 저장소의 'master' 브랜치에서도 변경 사항이 생긴 경우, 양 쪽의 변경을 통합할 필요가 있습니다.

![로컬 저장소의 'master' 브랜치에 변경 사항이 있는 경우](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup3_1_3.png)

이 때 pull 을 실행하여 소스를 병합할 수 있습니다. 충돌하는 변경이 없을 경우 자동적으로 병합 커밋이 만들어 지지만, 충돌이 있을 경우에는 충돌난 부분을 수동으로 해결한 다음 직접 commit 을 해 주어야 합니다.

![변경된 부분들에 서로 충돌이 없다면, 커밋은 자동으로 잘 처리될거야!](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup3_1_4.png)

----

## [fetch, 원격 저장소의 데이터를 로컬에 가져오기만 하기](https://backlog.com/git-tutorial/kr/stepup/stepup3_2.html)

pull 을 실행하면, 원격 저장소의 내용을 가져와 자동으로 병합 작업을 실행하게 됩니다. 그러나 단순히 원격 저장소의 내용을 확인만 하고 로컬 데이터와 병합은 하고 싶지 않은 경우에는 fetch 명령어를 사용할 수 있습니다.

fetch 를 실행하면, 원격 저장소의 최신 이력을 확인할 수 있습니다. 이 때 가져온 최신 커밋 이력은 이름 없는 브랜치로 로컬에 가져오게 됩니다. 이 브랜치는 'FETCH_HEAD'의 이름으로 체크아웃 할 수도 있습니다.

예를 들어, 로컬 저장소와 원격 저장소에 B에서 진행된 커밋이 있는 상태에서 fetch 를 수행하면 아래 그림과 같이 이력이 남겨집니다.

![로컬 저장소와 원격 저장소에B에서 분기된 커밋이 있는 상태에서 fetch 한 경우](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup3_2_1.png)

이 상태에서 원격 저장소의 내용을 로컬 저장소의 'master'에 통합하고 싶은 경우에는, 'FETCH_HEAD' 브랜치를 merge 하거나 다시 pull 을 실행하면 됩니다.

!['FETCH_HEAD'를 병합](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup3_2_2.png)

이렇게 fetch 후 merge 를 수행하면, pull 명령을 실행했을 때와 같은 이력이 만들어집니다. 사실 pull 이라는 것은 내부적으로 보면 fetch + merge 이기 때문이죠!

----

## [push, 로컬 저장소의 데이터를 원격 저장소로 밀어넣기](https://backlog.com/git-tutorial/kr/stepup/stepup3_3.html)

로컬 저장소에서 원격 저장소로 push(밀어넣기) 할 때에는, push 한 브랜치가 'fast-forward 병합' 방식으로 처리 되도록 지정해 둘 필요가 있습니다.

push 하지 않는 한 원격 저장소에 영향을 주지 않고 자신만의 브랜치에서 자유롭게 작업 할 수 있습니다. 그러나 로컬 저장소에서 작성한 브랜치를 공유하려면 명시적으로 원격 저장소로 push 해야 합니다.

![Push](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup3_3_1.png)

원격 저장소에서 모두가 공유하고 있는 커밋은 기본적으로 덮어쓰거나(overwrite) 임의로 변경해서는 안됩니다. 만약 그럴 경우, 그 원격 저장소와 동기화되어 있는 다른 저장소들의 이력에 모두 영향을 줄 테니깐요.

----

# 태그 (Tag)

## [태그 (Tag)](https://backlog.com/git-tutorial/kr/stepup/stepup4_1.html)

태그란, 커밋을 참조하기 쉽도록 알기 쉬운 이름을 붙이는 것을 말합니다.

한 번 붙인 태그는 브랜치처럼 위치가 이동하지 않고 고정됩니다.

Git 에서는 일반적으로 이름 정보만을 갖는 '태그(Lightweight tag)'와 보다 상세한 정보를 포함하는 '주석 태그(Annotated tag)', 이 두 가지 태그를 사용할 수 있습니다.

- 일반 태그(Lightweight tag)
    -   이름만 붙일 수 있어요
- 주석 태그(Annotated tag)
    -   이름을 붙일 수 있어요
    -   태그에 대한 설명도 포함할 수 있어요
    -   서명도 넣을 수 있어요
    -   이 태그를 만든 사람의 이름, 이메일과 태그를 만든 날짜 정보도 포함시킬 수 있어요

보통 '릴리스 브랜치(Release branch)'에서는 주석 태그를 사용하여 설명이나 서명을 넣은 보다 상세한 정보를 포함하는 태그를 사용하고, 로컬에서 일시적으로 사용하는 '토픽 브랜치(Topic branch)'에서는 이름만 만들어 붙이는 태그를 사용합니다.

![주석이 달린 태그, 경량 태그](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup4_1_1.png)

태그 이름을 지정하여 checkout 하거나 reset(아직 안 배웠어요!) 함으로써, 간단하게 과거의 특정 상태로 되돌릴 수 있답니다!

----

# 튜토리얼 2: 태그 사용하기

## [0. 사전 준비](https://backlog.com/git-tutorial/kr/stepup/stepup5_1.html)

로컬에「tutorial」이라는 이름으로 빈 폴더를 만들어 로컬 저장소로 등록해 봅시다.

```bash
$ mkdir tutorial
$ cd tutorial
$ git init
Initialized empty Git repository in /Users/eguchi/Desktop/tutorial/.git/
```

tutorial 폴더에 다음과 같은 내용의 myfile.txt 라는 이름으로 파일을 만든 후 커밋합니다.

```txt
원숭이도 이해할 수 있는 Git 명령어

$ git add myfile.txt
$ git commit -m "first commit"
[master (root-commit) a73ae49] first commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 myfile.txt
```

여기까지 진행했다면, 아래 그림과 같은 이력이 남게 됩니다.

![현재 시점의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup5_1_1.png)

----

## [1. 태그 추가하기](https://backlog.com/git-tutorial/kr/stepup/stepup5_2.html)

태그를 추가하려면 tag 명령어를 사용합니다. <tagname>에는 태그 이름을 지정합니다.

```bash
$ git tag <tagname>
```

현재 'HEAD'가 가리키고 있는 커밋에 'apple' 이라는 태그를 달려면, 다음과 같은 명령어를 실행합니다.

```bash
$ git tag apple
```

파라미터 없이 tag 명령어를 실행하면, 태그 목록을 볼 수 있습니다.

```bash
$ git tag
apple
```

또한 log 명령어에 --decorate 옵션을 붙여 실행하면, 태그 정보를 포함한 이력을 확인할 수 있습니다.

```bash
$ git log --decorate
commit e7978c94d2104e3e0e6e4a5b4a8467b1d2a2ba19 (HEAD, tag: apple, master)
Author: yourname <yourname@yourmail.com>
Date:   Wed Jul 18 16:43:27 2012 +0900

    first commit
```

![현재 HEAD가 가리키고 있는 커밋에 apple이라는 태그를 달기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup5_2_1.png)

----

## [2. 주석 달린 태그 추가하기](https://backlog.com/git-tutorial/kr/stepup/stepup5_3.html)

주석이 달린 태그를 추가하려면 tag 명령어에 -a 옵션을 지정하여 실행하면 됩니다. 엔터키를 눌러 실행한 후 태그에 대한 주석 내용을 바로 입력합니다. -m 옵션을 지정하여 명령어를 실행할 때에 바로 내용을 입력할 수도 있습니다.

```bash
$ git tag -a <tagname>
```

현재 'HEAD'가 가리키고 있는 커밋에 'banana'라는 주석이 달린 태그를 달려면 다음과 같이 명령어를 실행하면 됩니다.

```bash
$ git tag -am "누구나 쉽게 이해할 수 있는 Git 입문" banana
```

-n 옵션을 지정하여 tag 명령어를 실행하면 태그 목록과 주석 내용을 확인할 수 있습니다.

```bash
$ git tag -n
apple           first commit
banana          누구나 쉽게 이해할 수 있는 Git 입문
```

![현재 HEAD가 가리키고 있는 커밋에 banana라는 주석이 달린 태그를 달기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup5_3_1.png)

----

## [3. 태그 삭제하기](https://backlog.com/git-tutorial/kr/stepup/stepup5_4.html)

태그를 삭제하려면, tag 명령어에 -d 옵션을 지정하여 실행합니다.

```bash
$ git tag -d <tagname>
```

![태그를 삭제](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup5_4_1.png)

----

# 커밋 변경하기

## [이전에 작성한 커밋 수정하기](https://backlog.com/git-tutorial/kr/stepup/stepup6_1.html)

난이도 :  ![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)

--amend 옵션을 지정하여 커밋을 수행하면, 같은 브랜치 상에서 이전에 커밋했던 내용에 새로운 내용을 추가하거나 설명을 수정할 수 있습니다.

![이전에 작성한 커밋 수정하기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_1_1.png)

이럴 때 사용해 보세요 :

- 누락된 파일을 새로 추가하거나 기존의 파일을 업데이트 해야할 때
- 이전 커밋의 설명을 변경하고 싶을 때

----

## [이전에 작성한 커밋 지우기](https://backlog.com/git-tutorial/kr/stepup/stepup6_2.html)

난이도 :  ![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)

revert 명령어를 이용하면, 특정 커밋의 내용을 삭제할 수 있습니다. rebase -i 명령어나 reset 명령어를 통해 커밋을 삭제할 수도 있지만, 해당 커밋이 이미 공개된 상태인 경우에는 이러한 삭제 작업을 함부로 하기 어렵습니다. 이러한 경우에는 revert 명령어를 이용해서 특정 커밋의 내용을 지우는 새로운 커밋(B')을 만들어 보다 안전하게 처리할 수 있습니다.

아래 그림에서 보면, revert 명령어를 사용하여 커밋 B의 내용을 뒤집어 원래의 커밋 A의 상태로 돌아갈 수 있는 새로운 커밋 B'를 만들 수 있음을 알 수 있습니다.

![이전에 작성한 커밋 지우기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_2_1.png)

![이전에 작성한 커밋 지우기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_2_2.png)

이럴 때 사용해 보세요 :

- 이전에 작성한 커밋을 안전하게 지우고 싶을 때

----

## 커밋을 버리고 특정 버전으로 다시 되돌아가기

난이도 :  ![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)

reset 명령어를 이용하면 더 이상 필요 없어진 커밋들을 버릴 수 있습니다. 명령어 실행 시 어떤 모드로 실행할 지 지정하여 'HEAD' 위치와 인덱스, 작업 트리 내용을 함께 되돌릴지 여부를 선택할 수 있습니다.

![커밋을 버리고 특정 버전으로 다시 되돌아가기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_3_1.png)

모드는 기본적으로 'mixed'가 지정되며, 아래의 표에서와 같이 'soft'와 'hard' 중에서 선택할 수도 있습니다.

| 모드명 | HEAD의 위치 | 인덱스 | 작업 트리 |
| --- | --- | --- | --- |
| soft | 변경함 | 변경 안 함 | 변경 안 함 |
| mixed | 변경함 | 변경함 | 변경 안 함 |
| hard | 변경함 | 변경함 | 변경함 |

![커밋을 버리고 특정 버전으로 다시 되돌아가기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_3_2.png)

이럴 때 사용해 보세요 :

- 커밋만 되돌리고 싶을 때 (soft)
- 변경한 인덱스의 상태를 원래대로 되돌리고 싶을 때 (mixed)
- 최근의 커밋을 완전히 버리고 이전의 상태로 되돌리고 싶을 때 (hard)

----

## [다른 브랜치로부터 특정 커밋을 가져와서 내 브랜치에 넣기](https://backlog.com/git-tutorial/kr/stepup/stepup6_4.html)

난이도 :  ![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)

cherry-pick 을 이용하면 다른 브랜치에서 지정한 커밋을 복사하여 현재 브랜치로 가져올 수 있습니다.

![다른 브랜치로부터 특정 커밋을 가져와서 내 브랜치에 넣기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_4_1.png)

![다른 브랜치로부터 특정 커밋을 가져와서 내 브랜치에 넣기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_4_2.png)

이럴 때 사용해 보세요 :

- 특정 브랜치에 잘못 추가한 커밋을 올바른 브랜치로 옮기려고 할 때
- 다른 브랜치의 커밋을 현재 브랜치에도 추가하고 싶을 때

----

## [커밋 이력 편집하기](https://backlog.com/git-tutorial/kr/stepup/stepup6_5.html)

난이도 :  ![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)

rebase 명령어에 'i' 옵션을 지정하면 커밋을 다시 쓰거나 다른 커밋과 바꿔 넣을 수 있으며 특정 위치의 커밋을 삭제하거나 여러 커밋을 하나로 통합하는 작업을 할 수 있습니다.

![커밋 변경하기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_5_1.png)

![커밋 통합](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_5_2.png)

![커밋 이력 편집하기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_5_3.png)

이럴 때 사용해 보세요 :

- push 하기 전에 이전의 커밋 내용을 정리하고자 할 때
- 그룹으로 묶을 수 있는 커밋들을 알기 쉽게 하나로 통합하려고 할 때
- 이전 커밋에 누락된 파일들을 나중에 추가하고자 할 때

----

## [브랜치상의 커밋을 하나로 모아 병합한다](https://backlog.com/git-tutorial/kr/stepup/stepup6_6.html)

난이도 :  ![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)![☆](https://backlog.com/git-tutorial/kr/img/common/icon/ico_star.png)

이번에는 병합(merge) 할 때 사용할 수 있는, 조금 특별한 옵션인 '--squash'를 소개합니다.

이 옵션을 지정하여 브랜치를 병합하면 해당 브랜치의 커밋 전체를 통합한 커밋이 추가됩니다.

![squash 옵션](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_6_1.png)

![squash 옵션](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup6_6_2.png)

이럴 때 사용해 보세요 :

- 토픽 브랜치 안의 커밋을 한꺼번에 모아서 통합 브랜치에 병합하고자 할 때

----

# 튜토리얼 3: 커밋을 변경해보자!

## [1. commit --amend](https://backlog.com/git-tutorial/kr/stepup/stepup7_1.html)

이 튜토리얼에서는 사전에 이력이 준비되어 있는 로컬 저장소를 사용합니다.

[여기에서 다운로드](https://backlog.com/git-tutorial/kr/download/stepup-tutorial.zip)  해 주십시오.

이번 튜토리얼에서는 이전에 커밋한 내용을 수정해 보도록 하겠습니다.

위에서 다운로드 한 stepup-tutorial/tutorial1 폴더로 이동합니다. 이 저장소의 이력은 다음 그림과 같습니다.

![저장소 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_1_1.png)

log 명령어를 실행하여 이력을 확인합니다.

```bash
$ git log
commit 326fc9f70d022afdd31b0072dbbae003783d77ed
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:17:56 2012 +0900

    add의 설명을 추가

commit 48eec1ddf73a7fb508ef664efd6b3d873631742f
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:16:14 2012 +0900

    first commit
```

이제 sample.txt 파일을 열고 commit 의 설명을 추가합니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
commit: 인덱스의 상태를 기록하기
```

--amend 옵션을 이용하여 커밋합니다.

```bash
$ git add sample.txt
$ git commit --amend
```

열려진 편집기에서는 최근에 커밋한 내용이 포함되어 있을 것입니다. 내용을「add와 commit의 설명을 추가」로 바꾸어 넣은 다음 저장하고 빠져 나옵니다.

이로써 커밋의 내용이 수정 되었습니다. log 명령어에서 이력과 커밋 메시지를 확인해 봅니다.

![commit --amend](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_1_2.png)

```bash
$ git log
commit e9d75a02e62814541ee0410d9c1d1bf47ab1c057
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:17:56 2012 +0900

    add와 commit의 설명을 추가

commit 48eec1ddf73a7fb508ef664efd6b3d873631742f
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:16:14 2012 +0900

    first commit
```

----

## 2. revert

이 튜토리얼에서는 사전에 이력이 준비되어 있는 로컬 저장소를 사용합니다.

[여기에서 다운로드](https://backlog.com/git-tutorial/kr/download/stepup-tutorial.zip)  해 주십시오.

이번에는 revert 를 사용하여 「pull의 설명을 추가」를 지워보도록 하겠습니다.

위에서 다운로드 한 'stepup-tutorial/tutorial2' 폴더로 이동합니다. 이 저장소의 이력은 다음 그림과 같습니다.

![저장소 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_2_1.png)

log 명령어를 실행하여 이력을 확인합니다.

```bash
$ git log
commit 0d4a808c26908cd5fe4b6294a00150342d1a58be
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:19:26 2012 +0900

    pull의 설명을 추가

commit 9a54fd4dd22dbe22dd966581bc78e83f16cee1d7
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:19:01 2012 +0900

    commit의 설명 추가

commit 326fc9f70d022afdd31b0072dbbae003783d77ed
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:17:56 2012 +0900

    add의 설명을 추가

commit 48eec1ddf73a7fb508ef664efd6b3d873631742f
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:16:14 2012 +0900

    first commit
```

sample.txt 파일을 열어 내용을 확인합니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
commit: 인덱스의 상태를 기록하기
pull: 원격 저장소의 내용을 가져오기
```

revert 를 사용하여 'pull의 설명을 추가'하는 커밋을 취소합니다.

```bash
$ git revert HEAD
[master d47bb1d] Revert "pull의 설명을 추가"
 1 files changed, 1 insertions(+), 2 deletions(-)
```

sample.txt 를 열어 pull 의 설명이 지워졌는지 확인합니다.

![revert 이후 저장소의 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_2_2.png)

log 명령어를 실행하여 이력을 확인합니다.

```bash
$ git log
commit 7bcf5e3b6fc47e875ec226ce2b13a53df73cf626
Author: yourname <yourname@yourmail.com>
Date:   Wed Jul 18 15:46:28 2012 +0900

    Revert "pull의 설명을 추가"

    This reverts commit 0d4a808c26908cd5fe4b6294a00150342d1a58be.

commit 0d4a808c26908cd5fe4b6294a00150342d1a58be
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:19:26 2012 +0900

    pull의 설명을 추가

commit 9a54fd4dd22dbe22dd966581bc78e83f16cee1d7
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:19:01 2012 +0900

    commit의 설명 추가

commit 326fc9f70d022afdd31b0072dbbae003783d77ed
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:17:56 2012 +0900

    add의 설명을 추가

commit 48eec1ddf73a7fb508ef664efd6b3d873631742f
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:16:14 2012 +0900

    first commit
```

----

## [3. reset](https://backlog.com/git-tutorial/kr/stepup/stepup7_3.html)

이 튜토리얼에서는 사전에 이력이 준비되어 있는 로컬 저장소를 사용합니다.

[여기에서 다운로드](https://backlog.com/git-tutorial/kr/download/stepup-tutorial.zip)  해 주십시오.

이번에는 reset 을 사용하여 'master' 브랜치 앞의 두 개의 커밋을 삭제합니다.

위에서 다운로드 한 stepup-tutorial/tutorial3 폴더로 이동합니다. 이 저장소의 이력은 다음 그림과 같습니다.

![저장소 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_3_1.png)

log 명령어를 실행하여 이력을 확인합니다.

```bash
$ git log
commit 0d4a808c26908cd5fe4b6294a00150342d1a58be
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:19:26 2012 +0900

    pull의 설명을 추가

commit 9a54fd4dd22dbe22dd966581bc78e83f16cee1d7
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:19:01 2012 +0900

    commit의 설명 추가

commit 326fc9f70d022afdd31b0072dbbae003783d77ed
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:17:56 2012 +0900

    add의 설명을 추가

commit 48eec1ddf73a7fb508ef664efd6b3d873631742f
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:16:14 2012 +0900

    first commit
```

sample.txt 를 열어 내용을 확인합니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
commit: 인덱스의 상태를 기록하기
pull: 원격 저장소의 내용을 가져오기
```

reset 을 사용하여 커밋을 삭제합니다.

![commit를 삭제](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_3_2.png)

```bash
$ git reset --hard HEAD~~
HEAD is now at 326fc9f add의 설명을 추가
```

sample.txt 를 열어, commit 과 pull 의 설명이 지워졌는지 확인합니다. 또한 log 명령어를 실행하여 이력을 확인합니다.

```bash
$ git log
commit 326fc9f70d022afdd31b0072dbbae003783d77ed
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:17:56 2012 +0900

    add의 설명을 추가

commit 48eec1ddf73a7fb508ef664efd6b3d873631742f
Author: yourname <yourname@yourmail.com>
Date:   Mon Jul 16 23:16:14 2012 +0900

    first commit
```

reset 전의 커밋은 'ORIG_HEAD'라는 이름으로 참조할 수 있습니다. 실수로 reset 을 한 경우에는, 'ORIG_HEAD'로 reset 하여 reset 실행 전의 상태로 되돌릴 수 있습니다.

```bash
$ git reset --hard ORIG_HEAD
HEAD is now at 0d4a808 pull의 설명을 추가
```

----

## [4. cherry-pick](https://backlog.com/git-tutorial/kr/stepup/stepup7_4.html)

이 튜토리얼에서는 사전에 이력이 준비되어 있는 로컬 저장소를 사용합니다.

[여기에서 다운로드](https://backlog.com/git-tutorial/kr/download/stepup-tutorial.zip)  해 주십시오.

위에서 다운로드 한 stepup-tutorial/tutorial4 폴더로 이동합니다. 이 저장소의 이력은 다음 그림과 같습니다. 이번에는 다른 브랜치에서 수행한 「commit의 설명 추가」커밋 내용을 'master' 브랜치로 가져와 보도록 하겠습니다.

![저장소 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_4_1.png)

'master' 브랜치로 이동 한 후, cherry-pick 을 사용하여 「commit의 설명을 추가」한 커밋을 꺼내 'master'에 추가합니다. (문서 내의 커밋 "99daed2"와, 다운로드한 저장소 내의 커밋은 다를 가능성이 있습니다. 다운로드한 저장소 내에서 'git log'를 실행하여, 적절한 커밋을 확인하고 사용하세요. )

```bash
$ git checkout master
Switched to branch 'master'
$ git cherry-pick 99daed2
error: could not apply 99daed2... commit
hint: after resolving the conflicts, mark the corrected paths
hint: with 'git add <paths>' or 'git rm <paths>'
hint: and commit the result with 'git commit'
```

충돌이 발생했습니다. sample.txt 를 열고 충돌 부분을 수정한 후 커밋합니다.

```bash
$ git add sample.txt
$ git commit
```

----

## [5. rebase -i 로 커밋 모두 통합하기](https://backlog.com/git-tutorial/kr/stepup/stepup7_5.html)

이 튜토리얼에서는 사전에 이력이 준비되어 있는 로컬 저장소를 사용합니다.

[여기에서 다운로드](https://backlog.com/git-tutorial/kr/download/stepup-tutorial.zip)  해 주십시오.

위에서 다운로드 한 'stepup-tutorial/tutorial5' 폴더로 이동합니다. 이 저장소의 이력은 다음 그림과 같습니다. 이번에는 「commit의 설명을 추가」한 커밋과 「pull의 설명을 추가」한 커밋을 하나의 커밋으로 통합해 보도록 하겠습니다.

![저장소 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_5_1.png)

과거의 커밋을 통합할 때는 'rebase -i' 를 사용합니다.

```bash
$ git rebase -i HEAD~~
```

텍스트 에디터가 열리고 'HEAD'에서 'HEAD~~'까지의 커밋이 다음과 같이 표시됩니다.

```bash
pick 9a54fd4 commit의 설명 추가
pick 0d4a808 pull의 설명을 추가
```

```bash
## Rebase 326fc9f..0d4a808 onto d286baa
#
## Commands:
##  p, pick = use commit
##  r, reword = use commit, but edit the commit message
##  e, edit = use commit, but stop for amending
##  s, squash = use commit, but meld into previous commit
##  f, fixup = like "squash", but discard this commit's log message
##  x, exec = run command (the rest of the line) using shell
#
## If you remove a line here THAT COMMIT WILL BE LOST.
## However, if you remove everything, the rebase will be aborted.
#
```

두 번째 줄의 'pick' 문자를  squash로 변경하고 저장 · 종료합니다.

이로써 두 개의 커밋이 하나의 커밋으로 통합 되었습니다. log 명령어를 실행하여 이력을 확인합니다.

![커밋을 통합하기](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_5_2.png)

----

## [6. rebase -i 로 커밋 수정하기](https://backlog.com/git-tutorial/kr/stepup/stepup7_6.html)

이 튜토리얼에서는 사전에 이력이 준비되어 있는 로컬 저장소를 사용합니다.

[여기에서 다운로드](https://backlog.com/git-tutorial/kr/download/stepup-tutorial.zip)  해 주십시오.

위에서 다운로드 한 stepup-tutorial/tutorial6 폴더로 이동합니다. 이 저장소의 이력은 다음 그림과 같습니다. 이번에는 「commit의 설명을 추가」한 커밋을 수정해 보도록 하겠습니다.

![저장소 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_6_1.png)

'rebase -i' 를 사용하여 수정할 커밋을 선택합니다.

```bash
$ git rebase -i HEAD~~
```

텍스트 에디터가 열리고, 'HEAD'에서 'HEAD~~' 까지의 커밋이 다음과 같이 표시됩니다.

```
pick 9a54fd4 commit의 설명 추가
pick 0d4a808 pull 설명을 추가
```

```bash
## Rebase 326fc9f..0d4a808 onto d286baa
#
## Commands:
##  p, pick = use commit
##  r, reword = use commit, but edit the commit message
##  e, edit = use commit, but stop for amending
##  s, squash = use commit, but meld into previous commit
##  f, fixup = like "squash", but discard this commit's log message
##  x, exec = run command (the rest of the line) using shell
#
## If you remove a line here THAT COMMIT WILL BE LOST.
## However, if you remove everything, the rebase will be aborted.
#
```

첫 번째 줄의 'pick' 문자를 'edit'으로 변경하여 저장 · 종료합니다. 그러면 다음과 같은 출력 되고 수정할 커밋이 체크아웃된 상태가 됩니다.

```bash
Stopped at d286baa... commit의 설명 추가
You can amend the commit now, with

        git commit --amend

Once you are satisfied with your changes, run

        git rebase --continue
```

sample.txt 를 열어, commit 의 설명 부분을 적당히 변경합니다.

```txt
원숭이도 이해할 수 있는 Git 명령어
add: 변경 사항을 만들어서 인덱스에 등록해보기
commit: 인덱스의 상태를 저장하기
pull: 원격 저장소의 내용을 가져오기
```

commit  --amend 를 실행하여 변경한 내용을 저장합니다.

```bash
$ git add sample.txt
$ git commit --amend
```

commit 을 실행했다고 해서 rebase 작업이 끝난 것은 아닙니다. 이 커밋 작업이 종료했다는 것을 알리려면,  --continue 옵션을 지정하여 rebase 를 실행해야 합니다.

```bash
$ git rebase --continue
```

Note

이 때, 다른 커밋에서 충돌이 발생할 수 있습니다. 그럴 때에는 충돌 부분을 수정한 후 add 와 rebase  --continue를 실행하면 됩니다. 이 때, 커밋은 필요 없으므로 실행하지 않습니다. 만약 도중에 rebase 작업을 중지하고자 하는 경우에는 rebase에  --abort 옵션을 지정하여 실행하면 됩니다.

이제 커밋 수정이 완료 되었습니다.

Note

rebase 전의 커밋은 'ORIG_HEAD'라는 이름으로 남아 있습니다. 만약 rebase 한 후 원래대로 되돌리고자 하는 경우에는 'git reset --hard ORIG_HEAD'을 실행하여 rebase 전의 상태로 되돌릴 수 있습니다.

----

## [7. merge --squash](https://backlog.com/git-tutorial/kr/stepup/stepup7_7.html)

이 튜토리얼에서는 사전에 이력이 준비되어 있는 로컬 저장소를 사용합니다.

[여기에서 다운로드](https://backlog.com/git-tutorial/kr/download/stepup-tutorial.zip)  해 주십시오.

위에서 다운로드 한 stepup-tutorial/tutorial7 폴더로 이동합니다. 이 저장소의 이력은 다음 그림과 같습니다. 이번에는 'issue1' 브랜치의 모든 커밋을 하나의 커밋으로 병합하여 'master' 브랜치로 가져와 보도록 하겠습니다.

![저장소 이력](https://backlog.com/git-tutorial/kr/img/post/stepup/capture_stepup7_7_1.png)

'master' 브랜치로 이동한 후, '--squash' 옵션을 지정하여 merge 를 실행합니다.

```bash
$ git checkout master
Switched to branch 'master'
$ git merge --squash issue1
Auto-merging sample.txt
CONFLICT (content): Merge conflict in sample.txt
Squash commit -- not updating HEAD
Automatic merge failed; fix conflicts and then commit the result.
```

충돌이 발생했으므로, sample.txt를 열어 충돌 부분을 수정한 후 커밋합니다.

```bash
$ git add sample.txt
$ git commit
[master 0d744a7] Conflicts:   sample.txt
 1 files changed, 4 insertions(+), 0 deletions(-)
```

이로써 'issue1' 브랜치 상의 모든 커밋을 하나로 병합한 내용이 'master' 브랜치에 추가되었습니다. log 명령어를 실행하여 이력을 확인합니다.
