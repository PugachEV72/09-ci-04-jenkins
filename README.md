# Домашнее задание к занятию `10 «Jenkins»` - Пугач Евгений.


---

## `Подготовка к выполнению`

1. Создать два VM: для jenkins-master и jenkins-agent.
2. Установить Jenkins при помощи playbook.
3. Запустить и проверить работоспособность.
4. Сделать первоначальную настройку.

### Ответ:

`В Yandex Cloud было создано две машины:`

![Скриншот 1](https://github.com/PugachEV72/Images/blob/master/2024-01-28_15-59-20.png)

`Был запущен playbook:`

![Скриншот 2](https://github.com/PugachEV72/Images/blob/master/2024-01-28_16-05-03.png)

`Jenkins запущен, работоспособность проверена, настройка произведена:`

![Скриншот 3](https://github.com/PugachEV72/Images/blob/master/2024-01-28_16-12-37.png)

![Скриншот 4](https://github.com/PugachEV72/Images/blob/master/2024-01-28_18-56-54.png)

![Скриншот 5](https://github.com/PugachEV72/Images/blob/master/2024-01-28_21-53-34.png)

![Скриншот 6](https://github.com/PugachEV72/Images/blob/master/2024-01-28_21-54-04.png)

---

## `Основная часть`

1. Сделать Freestyle Job, который будет запускать molecule test из любого вашего репозитория с ролью.

### Ответ:

`Команды:`

![Скриншот 7](https://github.com/PugachEV72/Images/blob/master/2024-01-31_19-59-21.png)

`Сборка:`

![Скриншот 8](https://github.com/PugachEV72/Images/blob/master/2024-01-28_22-03-45.png)

`Dashboard:`

![Скриншот 9](https://github.com/PugachEV72/Images/blob/master/2024-01-28_22-04-32.png)

---

2. Сделать Declarative Pipeline Job, который будет запускать molecule test из любого вашего репозитория с ролью.

### Ответ:

`Скрипт:`

![Скриншот 10](https://github.com/PugachEV72/Images/blob/master/2024-01-31_20-07-50.png)

`Результат:`

![Скриншот 11](https://github.com/PugachEV72/Images/blob/master/2024-01-31_20-06-53.png)

`Перенос скрипта в репозиторий:`

![Скриншот 12](https://github.com/PugachEV72/Images/blob/master/2024-01-31_20-17-27.png)

![Скриншот 13](https://github.com/PugachEV72/Images/blob/master/2024-01-31_20-17-56.png)

![Скриншот 14](https://github.com/PugachEV72/Images/blob/master/2024-01-31_20-18-27.png)

`Результат:`

![Скриншот 15](https://github.com/PugachEV72/Images/blob/master/2024-01-31_20-15-49.png)

---

3. Перенести Declarative Pipeline в репозиторий в файл Jenkinsfile.

### Ответ:

[Jenkinsfile](https://github.com/PugachEV72/lighthouse-role/blob/master/Jenkinsfile)

---

4. Создать Multibranch Pipeline на запуск Jenkinsfile из репозитория.

### Ответ:

![Скриншот 16](https://github.com/PugachEV72/Images/blob/master/2024-01-31_22-02-49.png)

![Скриншот 17](https://github.com/PugachEV72/Images/blob/master/2024-01-31_22-03-53.png)

![Скриншот 18](https://github.com/PugachEV72/Images/blob/master/2024-01-31_22-13-03.png)

---

5. Создать Scripted Pipeline, наполнить его скриптом из pipeline.
6. Внести необходимые изменения, чтобы Pipeline запускал ansible-playbook без флагов --check --diff,  
   если не установлен параметр при запуске джобы (prod_run = True). По умолчанию параметр имеет  
   значение False и запускает прогон с флагами --check --diff.

### Ответ:

`Скрипт:`

![Скриншот 19](https://github.com/PugachEV72/Images/blob/master/2024-01-31_23-56-42.png)

`Результат:`

![Скриншот 20](https://github.com/PugachEV72/Images/blob/master/2024-01-31_23-23-31.png)

![Скриншот 21](https://github.com/PugachEV72/Images/blob/master/2024-01-31_23-24-06.png)

`True`

![Скриншот 22](https://github.com/PugachEV72/Images/blob/master/2024-01-31_23-25-08.png)

`False`

![Скриншот 23](https://github.com/PugachEV72/Images/blob/master/2024-01-31_23-26-18.png)

---

7. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл ScriptedJenkinsfile.

### Ответ:

[ScriptedJenkinsfile](https://github.com/PugachEV72/09-ci-04-jenkins/blob/main/ScriptedJenkinsfile)

---

8. Отправить ссылку на репозиторий с ролью и Declarative Pipeline и Scripted Pipeline.

### Ответ:

[ROLE](https://github.com/PugachEV72/lighthouse-role)

[Declarative Pipeline](https://github.com/PugachEV72/lighthouse-role/blob/master/Jenkinsfile)

[Scripted Pipeline](https://github.com/PugachEV72/09-ci-04-jenkins/blob/main/ScriptedJenkinsfile)

---

9. Сопроводите процесс настройки скриншотами для каждого пункта задания.

### Ответ:

`Dashboards:`

![Скриншот 24](https://github.com/PugachEV72/Images/blob/master/2024-02-01_00-03-50.png)

---

