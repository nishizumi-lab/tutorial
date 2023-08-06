# WSL2を有効化してUbuntuをインストールする方法

## WSL（Windows Subsystem for Linux）とは

WSL（Windows Subsystem for Linux）とは、Windows10上でLinuxを実行できる機能です。
Microsoft Store経由でアプリのようにLinuxのディストリビューションをインストールできます。
また、コマンドプロンプトからWSLのコマンドを呼び出しできます。

WSLには, WSL1とWSL2があり仕組みが大きく異ります. 本記事では後発でより互換性の高いWSL2について導入方法と使い方を紹介します.
なお, WSL2の特徴は以下のとおりです.

- 比較的メモリ消費量が少なく軽量
    0 WSL1よりはメモリを消費しますが, 他の仮想環境ソフトに比べてメモリ消費量が少ないです.そのため, メモリ不足になりにくく, 起動も早いです.
- 高い互換性
    0 Hyper-Vを利用してLinuxをエミュレーションしているため, WSL1よりも互換性が高くなっています.なお, WSL2に関するHyper-V機能はWindows10 Home版でも利用可能です.ただし, WSL2を使うときは, Hyper-Vを利用した他のソフトウェアは同時に利用できません.
- ファイルアクセス速度の向上
    - 仮想ドライブからext4を使用するため、直接やり取り出来るようになり, WSL1よりもアクセス速度が向上しています。

## WSL2の有効化

- ［スタート］アイコンを右クリック →［設定］→［アプリと機能］をクリックします。


- ［プログラムと機能］をクリックします。


- 左側のメニューから［Windowsの機能の有効化または無効化］をクリックします。

- 「Linux用Windowsサブシステム」にチェックを入れて［OK］をクリックします。

※古いバージョンのWindowsでは「Windows Subsystem for Linux」にチェックを入れて［OK］をクリックします。

- 再起動を要求されるので指示に従い再起動します。

- 管理者権限でコマンドプロンプトを開きます.

- 以下のコマンドを実行して「Virtual Machine Platform」を有効化します。

```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all
```

- PCの再起動をするか聞かれるのでYを入力して再起動します。

- WSL 2 Linux カーネルの更新ページの「x64 マシン用 WSL2 Linux カーネル更新プログラム パッケージ」をクリックして、WSL2用Linuxカーネルのインストーラをダウンロードして、インストールします。

- コマンドプロンプトを管理者権限で開き、以下を実行してWSLのデフォルトバージョンを2にします。

```
wsl --set-default-version 2
```

- 「For information on key differences with WSL 2 please visit https://aka.ms/wsl2」と表示されても気にせず進みます。

## WSL2上にUbuntuをインストールして実行

- スタートメニューから「Microsoft Store」アプリを起動します。

- 「linux」「ubuntu」などと検索するとインストール可能なLinuxディストリビューションの一覧が表示されます。
利用したいものを選んでインストールします。

- インストールしたLinuxディストリビューションは、スタートメニューに追加されたUbuntuアイコンから起動できます。

- 初回起動時、下記のような表示が出ます。インストールが完了するまでしばらく待ちます。

```
Installing, this may take a few minutes...
```

- インストールが完了すると、ユーザー名とパスワードの登録が求められます。
好きなユーザー名とパスワードを入力します。

```
Please create a default UNIX user account. The username does not need to match your Windows username.
For more information visit: https://aka.ms/wslusers
Enter new UNIX username: [ユーザー名]
Enter new UNIX password: [パスワード]
Retype new UNIX password:[パスワード（もう一回）]
passwd: password updated successfully
Installation successful!
To run a command as administrator (user "root"), use "sudo ".
See "man sudo_root" for details.
```

※Windows Subsystem for Linux (Ubuntu)は、Windowsの下記ディレクトリにインストールされます。

```
C:\Users\＜ユーザー名＞\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_*\LocalState\rootfs
```

- コマンドプロンプトで以下のコマンドを実行し、VERSIONが2になっていればWSL2でUbutnuを実行できます。

```
wsl -l -v
```
