# Увеличение размера витруального диска

### Учеличение размера виртуального диска средствами `VirtualBox`

1. Открываем консоль

2. Переходим в директорию в которую у нас установлен **VirtualBox**.

   Default:  `C:\Program Files\Oracle\Virtual Box`.  

3. Теперь получим информацию о нужном нам виртуальном диске `VDisk.vdi`:

   `VboxManage.exe showhdinfo C:\VMDISK\VDisk.vdi`

   Предполагается, что путь к нашим виртуальным дискам `C:\VMDISK` а нужный нам диск называется `VDisk.vdi`

   В результатах выводимых командой есть строка Logical size в которой указан максимальный размер диска. 

4. Теперь попробуем увеличить размер диска, к примеру, до 40 Гб (40960 Мб) командой:

   `VboxManage.exe modifyhd C:\VMDISK\VDisk.vdi −−resize 40960`

5. Еще раз выведем информацию о диске командой:

   `VboxManage.exe showhdinfo C:\VMDISK\VDisk.vdi`

   И убедимся что строка Logical size показывает новое значение максимально размера диска.

6. После увеличения максимального размера виртуального диска указанными выше командами нам необходимо зайти в гостевую систему и средствами гостевой операционной системы увеличить размер логического диска.