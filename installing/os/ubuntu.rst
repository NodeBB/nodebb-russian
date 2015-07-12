
Ubuntu
--------------------

Первым делом установим необходимое базовое программное обеспечение:

.. code:: bash

	$ sudo apt-get install git nodejs nodejs-legacy npm redis-server imagemagick build-essential


Если Вы хотите использовать MongoDB, LevelDB или другую базу данных вместо Redis, пожалуйста посмотрете раздел :doc:`Настройка Баз Данных <../../configuring/databases>`.

**Если менеджер пакетов может установить версию Node.js только ниже 0.8 (это относится к Ubuntu 12.10, 13.04), используйте команду ``node --version`` для определния версии  Node.js:**


.. code:: bash

	$ sudo add-apt-repository ppa:chris-lea/node.js
	$ sudo apt-get update && sudo apt-get dist-upgrade

Если Вы хотите установить Node.js v0.11, используйте репозиторий ``ppa:chris-lea/node.js-devel``.
Npm устанавливается вместе с nodejs

Затем клонируем этот репозиторий:


.. code:: bash

	$ git clone -b v0.7.x https://github.com/NodeBB/NodeBB.git nodebb


Получаем все необходимые зависимости для NodeBB:

.. code:: bash

    $ cd nodebb
    $ npm install --production


Запускаем Веб-установщик NodeBB и продолжаем установку в браузере по адресу http://127.0.0.1:4567.

.. code:: bash

    $ npm start

----

**Альтернативно**: Инициируйте скрипт настройки, запустив приложение с флагом ``setup``:


.. code:: bash

	$ ./nodebb setup


Настройки по умолчанию сделаны для локального сервера, который работает на дефолтном порту с базой данных redis на этой же машине, которая тоже слушает порт по умолчанию.

Теперь запускаем форум.


.. code:: bash

	$ ./nodebb start


NodeBB можно запускать с помощью вспомогательных программ, таких как ``forever``. :doc:`Посмотрите на возможные варианты здесь <../../running/index>`.
