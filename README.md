# Патч с Until к Python 2.7.15

Перед установкой данного патча, необходимо скачать исходный код Python 2.7.15, выполнив команду
```sh
git clone -b 2.7 --single-branch https://github.com/python/cpython.git
```

Далее скопировать патч `until.patch` В папку `cpython`
Перед применением патча проверить всё ли в порядке, командой:
```sh
git apply --check until.patch
```
Если команда не вернула ошибок, то применить патч:
```sh
git am --signoff < until.patch
```
После, следуя инструкциям Python собрать исходный код:
```sh
./configure
make
```
При успешной сборке, в каталоге появится исполняемый файл `python`

