# Marlin_3DP17_398
Added patches that can be built with ArduinoIDE 1.6.x

HICTOPのサイトで公開されているMarlinファームウエアのソースコードは、最近のArduinoIDEではビルドすることができませんでした。<p>
Youtubeにある動画では、ArduinoIDEを古い物にする手順が公開されていましたが、他のプロジェクトも持っているので、そうするのは難しいことです。<p>
また、Arduino AVR Boardsライブラリの1.6.11以前を入れると問題なくビルドできるようですが、上記と同じ理由で採用できません。<p>
調べてみると、stdio.hにfpos_tが定義されて、Marlinのfpos_tと名前空間がぶつかるのが原因のようでした。<p>
パッチを追加して、ビルドと書き込みができることを確認しました。<p>

Original:
　　Firmware - Hictop 3d printer
　　https://www.hic3dprinter.com/pages/firmware
