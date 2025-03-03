# Домашнее задание к занятию «Что такое DevOps. СI/СD» - Кощеев Иван

### Задание 1

**Что нужно сделать:**

1. Установите себе jenkins по инструкции из лекции или любым другим способом из официальной документации. Использовать Docker в этом задании нежелательно.
2. Установите на машину с jenkins [golang](https://golang.org/doc/install).
3. Используя свой аккаунт на GitHub, сделайте себе форк [репозитория](https://github.com/netology-code/sdvps-materials.git). В этом же репозитории находится [дополнительный материал для выполнения ДЗ](https://github.com/netology-code/sdvps-materials/blob/main/CICD/8.2-hw.md).
3. Создайте в jenkins Freestyle Project, подключите получившийся репозиторий к нему и произведите запуск тестов и сборку проекта ```go test .``` и  ```docker build .```.

В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

---

### Решение:

<details>

![image1](https://github.com/SirSeoPro/08-02/blob/main/img/1.png)
![image2](https://github.com/SirSeoPro/08-02/blob/main/img/2.png)
![image3](https://github.com/SirSeoPro/08-02/blob/main/img/3.png)

#### В том числе пришлось: 
1. По всем машинам добавить информацию в hosts, по резолву ubuntu-bionic
2. Добавить ползователя jenkins в группу docker
3. Репозитория на 8082 порту, http
4. Настройки nexus - realm - добавление в правый столбец "Docker Bearer Token Realm"

</details>

### Задание 2

**Что нужно сделать:**

1. Создайте новый проект pipeline.
2. Перепишите сборку из задания 1 на declarative в виде кода.

В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

---

### Решение:

<details>

![image4](https://github.com/SirSeoPro/08-02/blob/main/img/4.png)
![image5](https://github.com/SirSeoPro/08-02/blob/main/img/5.png)

</details>

### Задание 3

**Что нужно сделать:**

1. Установите на машину Nexus.
1. Создайте raw-hosted репозиторий.
1. Измените pipeline так, чтобы вместо Docker-образа собирался бинарный go-файл. Команду можно скопировать из Dockerfile.
1. Загрузите файл в репозиторий с помощью jenkins.

В качестве ответа пришлите скриншоты с настройками проекта и результатами выполнения сборки.

---

### Решение:

<details>

![image6](https://github.com/SirSeoPro/08-02/blob/main/img/6.png)
![image7](https://github.com/SirSeoPro/08-02/blob/main/img/7.png)

</details>
