# Домашнее задание к занятию "`8.3. GitLab`" - `Соловьев Д.В`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

`Приведите ответ в свободной форме........`

1. ![alt text](https://github.com/dsolovev455/8-03/blob/main/img/1.png)


---

### Задание 2

`Приведите ответ в свободной форме........`

1. ![alt text](https://github.com/dsolovev455/8-03/blob/main/img/2.png)


---

### Задание 3

`Приведите ответ в свободной форме........`

1.  https://github.com/dsolovev455/8-03/blob/main/gitlab-ci.yml

test:
  image: golang:1.16
  rules:
    - changes:
      - "*.go"
  script: 
   - go test .

static-analysis:
 image:
  name: sonarsource/sonar-scanner-cli
  entrypoint: [""]
 variables:
 script:
  - sonar-scanner -Dsonar.projectKey=MyProject -Dsonar.sources=. -Dsonar.host.url=http://192.168.0.190:9000 -Dsonar.login=sqp_fdbc3a7878b69b511c067d91c0993ea95de91b31

build:
  image: docker:latest
  script:
   - docker build .
   
![alt text](https://github.com/dsolovev455/8-03/blob/main/img/3.png)



!!!!!!
