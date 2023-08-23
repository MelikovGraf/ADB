# ADB

## Отобразить подключенный девайс в консоли.
 MacOS:    
 
    adb devices
 Windows: 
 
    .\adb devices

 ## Вывести адрес приложения todolist в системе Android.
  MacOS:  
  
    adb shell 'pm list packages -f' | grep reminder
  Windows: 
  
    .\adb shell 'pm list packages -f' | findstr reminder

 ## Установить .apk файл приложения todolist на телефон с компьютера через  ADB.
  MacOS:  
   
    adb install /Users/gr.debrin/Downloads/app-debug.apk 
  Windows: 
    
    .\adb install D:\download\app-debug.apk 
    
 ## Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.
  MacOS: 
  
    adb shell screencap /storage/emulated/0/DCIM/screen.png && adb pull /storage/emulated/0/DCIM/screen.png screen.png
  Windows: 
   
    .\adb shell screencap /storage/emulated/0/DCIM/screen.png && .\adb pull /storage/emulated/0/DCIM/screen.png screen.png

 ## Вывести в консоль логи приложения todolist.
  MacOS: 
    
    adb logcat | grep -nw "com.qrolic.reminderapp"
  Windows: 
  
    .\adb logcat -d | findstr com.qrolic.reminderapp

 ## Скопировать логи приложения todolist на компьютер.
  MacOS: 
    
    adb logcat | grep -nw "com.qrolic.reminderapp" > reminder.log
  Windows: 
    
    .\adb logcat -d | findstr com.qrolic.reminderapp > reminder.log

 ## Удалить приложение todolist с телефона через ADB.
  MacOS: 
    
    adb uninstall com.qrolic.reminderapp
  Windows: 
  
    .\adb uninstall com.qrolic.reminderapp
