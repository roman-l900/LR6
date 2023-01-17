# LR6
Лабораторная работа №6

**Цель работы:** изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

**Ход работы**

1.  Аккаунт github был создан до выполнения работы (ссылка - https://github.com/roman-l900).
    
2.  Сделана копия в личное хранилище (Fork).
![[Pasted image 20230117043955.png]]
      
3. Установил Git.
![[Pasted image 20230117044207.png]]
```sh
git --version
```
![[Pasted image 20230117044557.png]]
4. Настроен клиент git, а именно имя пользователя (Группа Фамилия И.О.) и email.
	
Изменено имя пользователя
```sh
git config --global user.name "4116 Лукин Р.С."
```
	![[Pasted image 20230117044924.png]]
	
Изменен email
```sh
git config --global user.email "romanl4116@gmail.com"
```
	 ![[Pasted image 20230117045059.png]]
	 
5. Клонирован свой личный удалённый репозиторий на компьютер с помощью команды git clone.
![[Pasted image 20230117045913.png]]
```sh
git clone https://github.com/roman-l900/LR6.git
```
![[Pasted image 20230117050147.png]]
6. Добавлен файл через интерфейс GitHub. Подтянуты изменения в локальный репозиторий.
	
Добавлен файл через интерфейс GitHub.
![[Pasted image 20230117051101.png]]
	
Подтянуты изменения в локальный репозиторий.
```sh
git pull
```
![[Pasted image 20230117052020.png]]
	
7. Получена история операций для каждой из веток.
	
Для master
```sh
git log
```
![[Pasted image 20230117052221.png]]
	
Для branch1
```sh
git log origin/branch1
```
![[Pasted image 20230117053239.png]]
8. Просмотрены последние изменения.
```sh
git status
```
![[Pasted image 20230117053559.png]]
9. Выполнено слияние в ветку master, разрешив конфликт.
	
Слияние веток
```sh
git merge branch1
```
![[Pasted image 20230117053834.png]]
	
Конфликт
![[Pasted image 20230117054858.png]]

Конфликт решен с помощью графического интерфейса.
![[Pasted image 20230117054830.png]]

 Зафиксированы изменения
```sh
git add mergefile.txt
git commit -m"conflict resolution"
```
 ![[Pasted image 20230117055349.png]]

10. Удалена побочная ветка после успешного слияния.

Локально
```sh
git branch -D branch1
```
![[Pasted image 20230117060105.png]]

На GitHub
```sh
git push origin -d branch1
```

11. Изменения сделаны и зафиксированы, оставляя комментарии,несколько раз. 

Первое изменене
![[Pasted image 20230117082126.png]]


Второе изменение
![[Pasted image 20230117082225.png]]

Третье изменение
![[Pasted image 20230117082318.png]]

Результат
![[Pasted image 20230117082532.png]]


12. Сделан откат коммита

```sh
git reset --hard HEAD~
```

До отката:
![[Pasted image 20230117082850.png]]

После отката:
![[Pasted image 20230117083044.png]]

Результат:
![[Pasted image 20230117082532.png]]

13. Создана ветка для отчета 
![[Pasted image 20230117083251.png]]

14. Получена история операций в форматированном виде
![[Pasted image 20230117083353.png]]
