
Ubuntu
--------------------

Esmalt paigaldame põhitarkvara:

.. code:: bash

	$ sudo apt-get install git nodejs redis-server imagemagick npm


Kui soovid kasutada MongoDB'd, LevelDB'd, või hoopiski mõnda muud andmebaasi peale Redis andmebaasi, siis uuri lähemalt :doc:`Andmebaasi konfigureerimine <../configuring/databases>` sektsioonist.

**Kui sinu Ubuntu package manager installis Node.js versiooni, mis on väiksem kui 0.8, tuleb manuaalselt uuendada uuemale versioonile. Esiteks tehke kindlaks Node.js versioon ``node --version``:**


.. code:: bash

	$ sudo add-apt-repository ppa:chris-lea/node.js
	$ sudo apt-get update && sudo apt-get dist-upgrade


Järgmise sammuna tuleb kloonida NodeBB Githubi repo sobivasse asukohta:


.. code:: bash

	$ git clone git://github.com/NodeBB/NodeBB.git nodebb


Paigaldame NodeBB foorumitarkvara:

.. code:: bash

    $ cd nodebb
    $ npm install


Käivitame NodeBB seadete muutmise režiimi ``setup`` flagiga:


.. code:: bash

	$ ./nodebb setup


Alseaded on mõledud local serveri jaoks, kus Redis andmebaas töötab samuti samas keskkonnas. 

Lõpetuseks tuleb foorum käivitada:


.. code:: bash

	$ ./nodebb start


NodeBB'd saab käivtada ka muude programmidega, näiteks ``supervisor`` ja ``forever``. :doc:`Vaata lähemalt siit <../../running/index>`.
