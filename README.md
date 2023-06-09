<<<<<<< HEAD
# lab09
=======
# lab9


Первым шагом является установка Vagrant на локальный компьютер.
```
vagrant -v
```

клониурем репозиторий лабы
```
git clone https://github.com/kkukuruz/lab09
cd lab9
git init
```

Создаём Vagrantfile
```
vagrant init
touch Vagrantfile
```

Настройка Vagrantfile

```
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provision :shell, path: "bootstrap.sh"
end
```


Создаём файл bootstrap.sh


```
#!/usr/bin/env bash

apt-get update
apt-get install -y apache2
cp /vagrant/index.html /var/www/html/
```
перед запуском вагранта нужно скачать virtualbox


Запуск виртуальной машины


```
vagrant up
```




Oстановка и удаление виртуальной машины


```
vagrant halt
vagrant destroy
```
>>>>>>> 32e4150 (Added files)
