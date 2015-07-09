
CentOS 6/7
--------------------

Во-первых, мы должны убедиться, что наш CentOS обновлен, мы можем сделать это, используя следующую команду:

.. code:: bash
	
	yum -y update

**Если Вы используете CentOS 7, то Вам необходимо установить epel release, это можно сделать выполнив следующую команду:

.. code:: bash
	
	yum -y install epel-release
	

Теперь мы установим базовое программное обеспечение:

.. code:: bash

	yum -y groupinstall "Development Tools"
	yum -y install nodejs git redis ImageMagick npm

Если Вы хотите использовать MongoDB, LevelDB или другую базу данных вместо Redis, пожалуйста посмотрете раздел :doc:`Настройка баз данных <../../configuring/databases>`.

Далее клонируем репозиторий:

.. code:: bash

	cd /path/to/nodebb/install/location
	git clone -b v0.7.x https://github.com/NodeBB/NodeBB nodebb
	
**Примечание: Для клонирования master-ветки Вы можте использовать такую же команду, убрав параметр "-b".

Получаем все зависимости, необходимые для NodeBB, после клонирования репозитория:

.. code:: bash
      
      cd nodebb
      npm install

Инициируем скрипт установки, запустив приложение с флагом ``setup``:

.. code:: bash

	  ./nodebb setup


Настройки по умолчанию сделаны для локального сервера, который работает на дефолтном порту с базой данных redis на этой же машине и тоже на дефолтном порту.

Наконец, мы запускаем форум.
  
.. code:: bash

	 ./nodebb start

NodeBB можно запускать с помощью вспомогательных программ, таких как forever ``forever``. :doc:`Посмотрите на возможные варианты здесь <../../running/index>`.
