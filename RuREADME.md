
<head>Установка OPT в Windows.</head>

<body>
1)  Скачайте "mingw-get-setup.exe" 


а)   c официального сайта:


     http://www.mingw.org/wiki/Getting_Started
     
     
     пролистать вниз, до:
     
     
     "1. Click on this mingw-get-setup.exe"
     
     
b)   с sourceforge :


     https://sourceforge.net/projects/mingw/files/Installer/
     
     
     кнопка "Download Latest Version"
     
     
	
2)	 Устанавите скачанный mingv на диск С. Не в "Program Files" или куда-либо еще. 


    По умолчанию правильный путь.
    
    
    Жмите "ОК" установка завершается и выходит диалоговое окно с настройками.
    
    
    Это окно закрыть.   
    
    

3)  Скачайте утилиту   Opt: http://509.ch/opt.7z


    Распакуйте ее в директорию С:/
    
    
    Можно просто скопировать архив с программой на диск С
    
    
    и правой кнопкой мыши выбрать "извлечь в текущую папку".
    
    

4)  Скачайте "NotePad++" и сразу же его установите.


    https://notepad-plus-plus.org/download/v7.7.html
    
    
   
3)  Запустите консоль.


    Пуск >> Выполнить >> пишем "cmd.exe"
    
    
	
4) 	В консоли пишем команды:


    cd C:\MinGW\bin
    
    
    mingw-get.exe update
    
    
    mingw-get.exe install mingwrt
    
    
    mingw-get.exe install w32api
    
    
    mingw-get.exe install binutils 
    
    
    mingw-get.exe install gcc 
    
    
    mingw-get.exe install g++
    
    
    mingw-get.exe install mingw32-make
    
    
    set PATH=C:\MinGW\bin;%PATH%
    
    
    cd C:\opt
    
    
    g++ -std=c++11 -O2 -DNDEBUG -DTASTENZAHL=35 -DENGLISH -static-libgcc -static-libstdc++ opt.cc -o opt
   
   
   
    Установка программы завершена. Не закрывайте консоль! Работать с программой будем в консоли.
	
	
	
5)  Не закрывая консоли откройте "NotePad++". В пункте меню "Кодировка" выберите "UTF-8".
    
    
    Теперь вставьте в этот документ текст, который хотите проанализировать. 
    
    
    Сохраните файл.
    
    
    В данном примере файл под названием "meinkorpus" c выбранным расширением "txt" 
	
	
	был сохранен в директории    "C:\opt".



6)  В консоли пишем команду :


opt meinkorpus.txt
	
	Теперь откройте "C:\opt". В списке файтов появились "meinkorpus.txt.1", "meinkorpus.txt.2", 
        "meinkorpus.txt.3" и "meinkorpus.txt.wl"
	Это файлы с программным анализом вашего текста.

    В качестве примера здесь приведена только одна из множества функций программы. 
    Возможности программы позволяют создавать кастомные прошивки с применением слоев
    под любые запросы. Смотрите руководство в архиве программы в pdf-файле "Anleitung.pdf".
    Во второй половине "Anleitung.pdf" руководство на английском языке. 	
</body> 
