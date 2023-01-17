# LR6
Лабораторная работа №6

**Цель работы:** изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

**Ход работы**

1.  Аккаунт github был создан до выполнения работы (ссылка - https://github.com/roman-l900).
    
2.  Сделана копия в личное хранилище (Fork). ![Pasted image 20230117043946](https://user-images.githubusercontent.com/122844695/212819066-32487817-ad9f-4bf1-acb9-300ed8464080.png)

      
 
 3. Установил Git.

![Pasted image 20230117044207](https://user-images.githubusercontent.com/122844695/212819099-7677579b-48bc-43a9-837d-daf527abc59e.png)


```sh
git --version
```
![Pasted image 20230117044557](https://user-images.githubusercontent.com/122844695/212819145-e73ba4cc-b4be-47f8-9bf8-52bd71359e59.png)
4. Настроен клиент git, а именно имя пользователя (Группа Фамилия И.О.) и email.
	
Изменено имя пользователя
```sh
git config --global user.name "4116 Лукин Р.С."
```
![Pasted image 20230117044924](https://user-images.githubusercontent.com/122844695/212819219-ebca3bb2-b602-4d24-b14b-c8e681b72ec4.png)
	
Изменен email
```sh
git config --global user.email "romanl4116@gmail.com"
```
![Pasted image 20230117045059](https://user-images.githubusercontent.com/122844695/212819261-465ec0ba-4679-4ded-9d99-28893f34ac7a.png)
	 
5. Клонирован свой личный удалённый репозиторий на компьютер с помощью команды git clone.
![Pasted image 20230117045913](https://user-images.githubusercontent.com/122844695/212819300-87c30cfb-a60f-48a9-b839-c3420f995682.png)
```sh
git clone https://github.com/roman-l900/LR6.git
```
![Pasted image 20230117050147](https://user-images.githubusercontent.com/122844695/212819319-efb99c36-764e-4894-b18c-746d4c2698e8.png)


 6. Добавлен файл через интерфейс GitHub. Подтянуты изменения в локальный репозиторий.
	
 Добавлен файл через интерфейс GitHub.

![Pasted image 20230117051058](https://user-images.githubusercontent.com/122844695/212819343-47606ae7-4e4d-4ec4-b24d-5d08fe47b787.png)
	
Подтянуты изменения в локальный репозиторий.
```sh
git pull
```
![Pasted image 20230117052020](https://user-images.githubusercontent.com/122844695/212819363-d90c3aff-3f1c-45df-9aa4-239694c19ef0.png)
	
7. Получена история операций для каждой из веток.
	
Для master
```sh
git log
```
![Pasted image 20230117052221](https://user-images.githubusercontent.com/122844695/212819394-5f2c2363-1e89-49ca-a94d-6d490528b3a7.png)
	
Для branch1
```sh
git log origin/branch1
```
![Pasted image 20230117053239](https://user-images.githubusercontent.com/122844695/212819435-845d0d59-7351-4cfd-8742-d5e9675f0636.png)

 8. Просмотрены последние изменения.
```sh
git status
```
![Pasted image 20230117053557](https://user-images.githubusercontent.com/122844695/212819456-78f643f9-9634-4272-a38e-7f377bd401d6.png)
 
 9. Выполнено слияние в ветку master, разрешив конфликт.
	
Слияние веток
```sh
git merge branch1
```
![Pasted image 20230117053559](https://user-images.githubusercontent.com/122844695/212819485-f69aeb84-c615-46d4-a76f-1e58826b73d1.png)
	
 
 
 
 Конфликт

![Pasted image 20230117053834](https://user-images.githubusercontent.com/122844695/212819559-4af99908-b9cf-45d8-8a00-e23c0cc18b9c.png)



Конфликт решен с помощью графического интерфейса.

![Pasted image 20230117054830](https://user-images.githubusercontent.com/122844695/212819579-8abd663d-d08f-4fc8-9895-1a6384c16c9a.png)

 
 Зафиксированы изменения
```sh
git add mergefile.txt
git commit -m"conflict resolution"
```
 ![Pasted image 20230117055349](https://user-images.githubusercontent.com/122844695/212819624-92d0ae86-04f9-4645-9660-2b3bc073c75f.png)

10. Удалена побочная ветка после успешного слияния.

Локально
```sh
git branch -D branch1
```
![Pasted image 20230117060105](https://user-images.githubusercontent.com/122844695/212819652-dabd2dd3-4c78-4e98-835c-271385e0a86c.png)

На GitHub
```sh
git push origin -d branch1
```

11. Изменения сделаны и зафиксированы, оставляя комментарии,несколько раз. 

Первое изменене

![Pasted image 20230117071355](https://user-images.githubusercontent.com/122844695/212819806-2dda59b1-ac5a-4ec7-bb8f-e9bf3a39aff9.png)


 Второе изменение

![Pasted image 20230117071635](https://user-images.githubusercontent.com/122844695/212819824-b9d80570-8924-43d5-b4f6-2e497f269124.png)

 Третье изменение

![Pasted image 20230117071912](https://user-images.githubusercontent.com/122844695/212819838-c6e560f9-9694-4c3e-a51a-e9a94fb23299.png)

 Результат

![Pasted image 20230117082532](https://user-images.githubusercontent.com/122844695/212819873-9a710d08-698f-4215-b1fa-90ebd810ccd4.png)


 
 12. Сделан откат коммита

```sh
git reset --hard HEAD~
```

 
 До отката:
 
![Pasted image 20230117082828](https://user-images.githubusercontent.com/122844695/212819913-3a7eec97-699c-41a1-b8ce-b668e8f668a4.png)

 После отката:

![Pasted image 20230117083044](https://user-images.githubusercontent.com/122844695/212819949-3593b6bf-bf01-40c9-a06c-f75d67dbcc5e.png)

 Результат:

![Pasted image 20230117082850](https://user-images.githubusercontent.com/122844695/212820054-a3663670-2c52-4cd6-b445-1980b1dd7cd2.png)


 13. Создана ветка для отчета 

![Pasted image 20230117083251](https://user-images.githubusercontent.com/122844695/212820016-3eed0195-a3be-4d4e-89a2-1e1ace225ab7.png)

 14. Получена история операций в форматированном виде

![Pasted image 20230117083353](https://user-images.githubusercontent.com/122844695/212820074-10bfee3b-b1b3-4d66-b424-aac7524aaa21.png)
