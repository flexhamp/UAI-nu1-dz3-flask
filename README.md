# Развертывание приложения

## Настройка приложения на сервере
1. ##### Клонируем
    ```shell script
    git https://github.com/flexhamp/UAI-nu1-dz3-flask.git
    cd UAI-nu1-dz3-flask
    ```
2. ##### Создаем виртуальное окружение
    ```shell script
    virtualenv venv --python=python3.8
    # Активируем окружение
    source venv/bin/activate
    python -V
    # Устанавливаем зависимости
    pip install -r requirements.txt
    # Проверим запустив
    python main.py
    ```

## Установка Установка Python 3.8 в CentOS 8
```shell script
dnf groupinstall 'development tools'

dnf install bzip2-devel expat-devel gdbm-devel \
    ncurses-devel openssl-devel readline-devel \
    sqlite-devel tk-devel xz-devel zlib-devel wget

wget https://www.python.org/ftp/python/3.8.5/Python-3.8.5.tgz

tar -xf Python-3.8.5.tgz

cd Python-3.8.5
./configure --enable-optimizations

# Измените -j, чтобы соответствовать количеству ядер в вашем процессоре. Вы можете найти номер, набрав nproc.
$make -j 4

make altinstall
```

## Установка Установка Python 3.8 в CentOS 7
```shell script
yum -y groupinstall "Development Tools"

yum -y install openssl-devel bzip2-devel libffi-devel wget

wget https://www.python.org/ftp/python/3.8.5/Python-3.8.5.tgz

tar -xf Python-3.8.5.tgz

cd Python-3.8.5
./configure --enable-optimizations

make altinstall

python3.8 --version
# Python 3.8.5

pip3.8 --version
# pip 20.1.1 from /usr/local/lib/python3.8/site-packages/pip (python 3.8)
```