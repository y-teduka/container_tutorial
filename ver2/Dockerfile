# 0.ubuntu:2204をベースにする
FROM ubuntu:22.04

# 1.command_tutorialディレクトリをルートディレクトリに作榮して
#　　そのなかにFirstvi.txtを作成
RUN mkdir /command_tutorial
RUN touch /command_tutorial/firstvi.txt

# 2.viのインストール
RUN apt-get update
RUN apt-get -y install vim

# 3. ubuntuの日本語対応
RUN apt-get -y install language-pack-ja
RUN update-locale LANG=ja_JP.utf8
ENV LANG ja_JP.utf8

# 4.日本時間(JST)の設定
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install tzdata
RUN echo 'Asia/Tokyo' > /etc/timezone
ENV TZ Asia/Tokyo