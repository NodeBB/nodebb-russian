OSX Mavericks
==========

Необходимое программное обеспечение
------------------------------------

В начале установим следующие программы:

* http://nodejs.org/
* http://brew.sh/




Запуск NodeBB
---------------------

Установите redis с homebrew:

.. code::

  brew install redis
  
Запускаем redis server, введите в терминале:
  
.. code::

  redis-server

Клонируем репозиторий NodeBB:

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

    ./nodebb setup

Можно оставить все опции по умолчанию.

Готово! Запускаем после установки 

.. code:: bash

    ./nodebb start

Можно проверить работу форума по адресу ``http://localhost:4567/``


