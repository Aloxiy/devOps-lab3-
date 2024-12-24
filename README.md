Сначала на своем ноутбуке скачал vault
![image](screens/1.png)
Дальше я запустил Vault в dev-режиме
![image](screens/2.png)
Дальше я экспортировал переменные среды для CLI:
![image](screens/3.png)

Дальше я настроил секрет Vault
![image](screens/4.png)


Дальше я начал устанавливать токен Vault в GitHub Secrets и понял, что в чужом репозитории у меня нет прав заходить в настройки. Поэтому данная лаба выполнена в другом репозитории.
В своем уже репозитории я зашел в настройки и добавил токен

![image](screens/5.png)

Теперь я создал в папке workflows файл vault-integration.yml

![image](screens/6.png)

Зашел в Actions и понял, что Vault я настраивал локально, а Github Actions запускает workflow в своей облачной инфраструктуре...

Я нашел решение этой проблемы с помощью запуска Vault с помощью docker в Github Actions

