# lab09


Первым шагом является установка Vagrant на локальный компьютер.
```
vagrant -v
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

apt-get update
apt-get install -y apache2
cp /vagrant/index.html /var/www/html/
```
перед запуском вагранта нужно скачать virtualbox
![изображение](https://github.com/Wenir04/lab9/assets/113133600/a151ed24-79a3-4b15-b114-057e9bd019ab)


Запуск виртуальной машины


```
vagrant up
```

![Снимок экрана 2023-06-02 190121](https://github.com/dandelion16012/lab09/assets/114254438/fb4633ef-4124-4f26-bd31-9d209011dc6c)



Oстановка и удаление виртуальной машины


```
vagrant halt
vagrant destroy
```

команда для быстрого подключения к серверу
```
vagrant ssh
```
 
