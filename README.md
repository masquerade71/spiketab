//ssh настройка
sudo apt install openssh-server -y
sudo systemctl enable ssh
sudo ufw allow ssh
sudo systemctl status ssh         // на фотку


// УДАЛЕННЫЙ ДОСТУП
gsettings set org.gnome.desktop.remote-desktop.vnc auth-method "password"
gsettings set org.gnome.desktop.remote-desktop.vnc view-only false

gsettings set org.gnome.desktop.remote-desktop.rdp enable true
gsettings set org.gnome.desktop.remote-desktop.vnc enable true

sudo apt install gnome-remote-desktop -y

systemctl --user enable gnome-remote-desktop
systemctl --user start gnome-remote-desktop

systemctl --user status gnome-remote-desktop     // НА ФОТКУ


//БАЗОВОЕ ПО
sudo dnf install libreoffice // скачиваем libreoffice
sudo dnf install gimp

//принтер
sudo apt install -y cups cups-pdf //принтер

//РЕЗЕРВНОЕ КОП(ВОЗМОЖНО НА ВАШЕЙ ВЕРСИИ НАДО С ОДНИМ ТИРЕ)
sudo tar cvpzf /backup.tgz --exclude=/proc --exclude=/lost+found --exclude/=backup.tgz --exclude=/mnt --exclude=/sys --exclude=/web --exclude=/media /


//Создан установочный образ системы
sudo dd if=/dev/sda of=/home/pasha/ubuntu_backup.iso bs=4M status=progress    //ПУТЬ САМИ УКАЖИТЕ КУДА СОХРАНЯТЬ(ДЕЛАЙТЕ ВО ВТОРОМ ТЕРМИНАЛЕ)

//точка восстановы
sudo apt install timeshift -y 
sudo timeshift --create //ДЕЛАЙТЕ ВО ВТОРОМ ТЕРМИНАЛЕ ТК ЭТО ДОЛГО

//Группы пользователей 
sudo apt install gnome-system-tools //утилита для создания групп
ЧТОБЫ СОЗДАТЬ ПОЛЬЗОВАТЕЛЯ ЗАЙТИ В НАСТРОЙКИ -СИСТЕМА -ДОБАВИТЬ НОВОГО НЕ ДАВАТЬ ЕМУ ПРАВА АДМИНА ДОБАВИТЬ ПАРОЛЬ - ЗАЙТИ В ПРОГРАММУ ПОЛЬЗОВАТЕЛИ И ГРУППЫ - ПОТЫКАТЬ ДОБАВИТЬ ПОЛЬЗОВАТЕЛЯ С ПРАВАМИ ТО ЕСТЬ РУТА В ГРУППУ АДМИНОВ А ПОЛЬЗОВАТЕЛЯ БЕЗ ПРАВ В ГРУППУ ЮЗЕРОВ И ВОТ ВЫ ВЫПОЛНИЛИ ВСЕ ЗАДАНИЯ ПО ПОЛЬЗОВАТЕЛЯМ

// Журнал мониторинга
sudo apt install auditd -y
sudo auditctl -w /etc/passwd -p wa -k passwd_changes
sudo ausearch -k passwd_changes
sudo systemctl status auditd // НА ФОТКУ



//антивирус
sudo apt install fail2ban
sudo systemctl enable fail2ban
sudo systemctl start fail2ban
sudo systemctl status fail2ban //для скрина что робит

//МЕИН ЗАДАНИЕЕЕЕЕЕЕЕЕЕЕЕЕЕЕЕ

//ide
vscode

//3d графика
blender

//антивирус
sudo apt install fail2ban
sudo systemctl enable fail2ban
sudo systemctl start fail2ban
sudo systemctl status fail2ban //для скрина что робит


//api графический дизайнер для 3d 
sudo apt install vulkan-tools libvulkan-dev vulkan-validationlayers -y //vulkan

// Система контроля версий
sudo apt install git git-cola -y         //git с gui

//////////////
- приложения, разработанные для работы с ограниченной цветовой палитрой, корректно отображаются       //СКАЧАТЬ ВСЕ ПРОГРАММЫ + БИБЛИОТЕКИ ИТД ИЗ КРАСНОГО ЗАДАНИЯ
  
- приложения, разработанные для работы с низким разрешением, корректно отображаются              //ПРОСТО ЗАЙТИ В ПРОГУ И ЗАСКРИНИТЬ, ЧТО ВСЕ ОТОБРАЖАЕТСЯ КОРРЕКТНО (ИНСТРУМЕНТЫ КНОПОЧКИ ИТД)

- выполнена настройка обмена данными с другими системами    // ЭТО ЗНАЧИТ, ЧТО МОЖНО ЭКСПОРИТРОВАТЬ ФАЙЛ(ПОЭТОМУ ВЫБИРАЙТЕ ПРИЛОЖЕНИЯ С ЭТИМИ ФУНКЦИЯМИ) МОЖНО ДЛЯ ВИДА ЭКСПОРТИРОВАТЬ

- приложения, разработанные для работы с низким разрешением, кор-ректно отображаются         // ПОМЕНЯТЬ РАЗРЕШЕНИЕ С 16:9 НА 1200Х800 +- ЗАЙТИ В ПРОГУ И ПРОВЕРИТЬ ЧТО ВСЕ КЛИКАБЕЛЬНО И ПРОГРАММА КОРРЕКТНО ПОДСТРОИЛАСЬ ПОД РАЗРЕШЕНИЕ
- решены проблемы с отображением меню и кнопок   //ЕСЛИ ЧТО ТО ПЛОХО ИЗМЕНИТЬ МАСШТАБ НА 100

- отключена композиция рабочего стола
  gsettings set org.gnome.mutter experimental-features "[]"
  gsettings set org.gnome.desktop.interface enable-animations false

  запустить glxgears  не должно быть разрывов и ступенек окно плавно передвигается
  

- отключено масштабирование изображения при высоком разрешении экрана   //ЗДЕСЬ ПРОСТО ЗАСКРИНИТЬ В ПАРАМЕТРАХ ЭКРАНА ЧТО МАСШТАБ = 100 И ВЫКЛЮЧЕНО ДРОБНОЕ МАСШТАБИРОВАНИЕ



  


