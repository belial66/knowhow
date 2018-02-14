Windows Server 2016 Hyper-V のハードウェア要件
===============================================
https://docs.microsoft.com/ja-jp/windows-server/virtualization/hyper-v/System-requirements-for-Hyper-V-on-Windows

Hyper-Vは仮想化のため、多くのコンピューターリソースを使うので、Windows Server 2016よりも多くの要件をがある。
既にHyper-Vを使っているなら、既存のハードウェアをそのまま使えるだろう。
一般的に、Windows Server 2012 R2の要件とそう変わりはないが、Shielded virtual machine もしくは discrete device assignmentを使うには、新たな要件が必要となってくる。

必須要件
--------------------
* ハイパーバイザーのインストールには、SLAT対応の64bitプロセッサが必須。
  ただし、Hyper-Vマネージャ、PowerShellのHyper-Vコマンドレットのようなツール利用には要求されない。
* VM Monitor Mode Extension
* 十分なメモリ量。少なくとも4GB。
* 仮想化サポート
  - ハードウェアの仮想化支援機構
    IntelはIntel Virtualization Technology(Intel-VT)、AMDはAMD Virtualization(AMD-V)
  - Hardware-enforced Data Execution Prevention (DEP)
    IntelはXD bit(execute disable bit)、AMDはNX bit(non execute bit)

要件を満たしているかの確認方法
------------------------------
ホストのコマンドプロンプトか、PowerShell上で、「SystemInfo.exe」を実行する。
既に、Hyper-Vがインストール済みの場合は、確認できない。



