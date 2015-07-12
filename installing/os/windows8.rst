Windows 8
==========

Необходимое программное обеспечение
---------------------------------------

В начале установим следующие программы:

* https://windows.github.com/
* http://nodejs.org/
* http://sourceforge.net/projects/redis/files/redis-2.6.10/
* http://imagemagick.org/script/binary-releases.php#windows/
* https://www.python.org/ftp/python/2.7.8/python-2.7.8.msi

Возможно Вам придется перезагрузить компьютер.

Запуск NodeBB
---------------------

Запускаем Redis Server

.. note::

	Расположение Redis Server по умолчанию:

	**C:\\Program Files (x86)\\Redis\\StartRedisServer.cmd**

Откройте Git Shell и введите следующие команды. Клонируем репозиторий NodeBB:

.. code:: bash

    git clone -b v0.7.x https://github.com/NodeBB/NodeBB.git

Заходим в каталог: 

.. code:: bash

    cd NodeBB

Устанавливаем зависимости:

.. code:: bash

    npm install

Запускаем интерактивную установку:

.. code:: bash

    node app.js --setup

Можно оставить все параметры по умолчанию.

Готово! После установки, запустите: 

.. code:: bash

    node app.js

Можно проверить работу форума по адресу ``http://127.0.0.1:4567/``


Разработка под  Windows
-------------------------

Каждый раз когда Вы делаете изменения, выключение и перезагрузка NodeBB будет головной болью. Для начала установим supervisor:

.. code:: bash

    npm install -g supervisor

Откройте bash:

.. code:: bash

    bash

И запустите NodeBB в режиме "watch":

.. code:: bash

    ./nodebb watch

Эта команда запустит NodeBB в режиме разработчика, будет отслеживать изменения файлов и автоматически перезапускать форум.
