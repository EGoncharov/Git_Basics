### List of basic commands and rules when working with git


	clear — Очистить консоль

**Навигация**

	pwd — показать текущий каталог
	ls - показать файлы в данной папке, кроме скрытых
	ls -f — показать файлы в данной папке, включая и скрытые
	cd c:/ — перейти в конкретный каталог
	cd - — вернуться назад
	cd .. — выйти на 1 уровень вверх
	cd ../.. — выйти на 2 уровня вверх

**Создание каталогов**

	mkdir — Создать папку
	cd !$ — Перейти в только что созданную папку
	mkdir -p {app1,app2} — Создать сразу несколько папок
	mkdir -p app/{css,js} — Создать сразу несколько вложенных папок

**Создание файлов**

	touch index.html — Создать файл index.html
	touch app/{css/main.css,js/main.js,index.html} — Создать сразу несколько файлов, никаких лишних пробелов быть не должно

**Удаление файлов**

	touch — позволяет создавать файлы
	remove xxx - удаление xxx файла
	rm test — Удалить пустую папку test
	rm -r test — Удалить папку test с файлами внутри неё

	mv app1/*.* app2 — Переместить все файлы из папки app1 в папку app2
	cat xxx - показывает содержимое файла xxx
	git config --global --list - настройка имени, почты и т.д.
	git status - показывает внесенные изменения
	git commit - i (пишем назв изменения) - esc :wq (внести изменен и записать)
	git commit --amend - это изменение название коммита если вы не запушили изменения
	git log - история комитов
	git revert xxx... - xxx это хэш коммита к которому нужно откатиться (созд новый коммит)
	git reset xxx - возврат к ххх коммиту (новый коммит не созд)
	git reset --soft / git reset --mixed - можно откатиться на другой коммит без изменений рабочей директории

	vi namefile - открывает файл для изменений
		i - вносить изменения
		esc - выйти из редактирования
		:wq - сохранить изменения

	git clone xxx - клонирует xxx (репозиторий) на комп
	git branch - какие ветки есть
	git branch xxx - создание новой ветки
	git branch -d xxx - удаление ветки ххх
	git checkout xxx - xxx это назв ветки/коммита на которую переходим
	git checkout -b xxx - создание ветки ххх и сразу переход на неё

	git merge xxx 
		Коммиты из двух веток сливаются в одну ветку по дате коммита, в конце ветки, которую произошло слияние,
		появится новый merge commit (пример замок)
	git merge master xxx - изменения в ветке мастера мержаться в ветку ххх

	git fetch - ?
	git pull origin master - изменения на гите и локалке пушаться и мержаться на ветке master
	git push origin master - добавление изменений после git commit
	git stash / git stash pop - скрытие и возврат файлов, предварительно git add
	git stash drop - удаление скрытых файлов

	git rebase 
		перезапись истории текущей ветки, которая будет начинаться от конца ветки-родителя,
		которая указана аргументом в команде git rebase

	git rebase -i 
		* Позволяет перезаписать историю ветки-родителя, начиная с того коммита, откуда произошло ветвление текущей ветки
		* Позволяет редактировать изменения в одном или нескольких коммитах из заданного диапазона коммитов
		* Позволяет слить коммиты из ветки-родителя в текущую по дате добавления

	.gitignore - файл в котором указываешь что не нужно пушить на гит
	git mv file_from file_to - переименновать файл

**Main command set**

	git clone xxx
	cd xxx
	npm install
	npm test
	git add .
	git commit -m "xxx"
	git push origin master
​
