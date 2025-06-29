[[Golang]]
Установила [[WSL]] в командной строке
wsl --install

Обновила все через Linux-терминал
sudo apt-get update && sudo apt-get upgrade -y

удалить го
which go #оттуда скопировать путь
sudo rm -rf /usr/local/go
nano ~/.bashrc #оттуда убрать все упоминания го

установить го
wget https://dl.google.com/go/go1.24.1.linux-amd64.tar.gz
sudo tar -xvf go1.24.1.linux-amd64.tar.gz
sudo mv go /usr/local
Прописываю путь к го
nano ~/.bashrc
#вставить в файл в конец
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export PATH=$GOPATH/bin:$GOROOT/bin:$PATH

В cmd закрыть wsl
wsl --shutdown

/////////////////////
Переустановить wsl
1. Удалить убунту в программах
2.Open the Control Panel and go to 
Programs -> Turn Windows Features On or Off.
Uncheck the Windows Subsystem for Linux option there
and click OK
3.
wsl --install
перезагрузить пк
wsl --unregister ubuntu
wsl --install
завести пользователя
exit