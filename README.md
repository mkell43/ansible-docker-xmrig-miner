Docker Xmrig Miner
==================

A role to deploy a xmrig docker container onto a host.

Requirements
------------

This role has only been tested on Ubuntu 16.04 (Xenial), use anywhere else at your own risk.  Or, even better, submit a pull request with fixes that got it working on your platform.

Expects docker to be installed on the host.  Brings what it needs to manage containers with it.

Role Variables
--------------

All of these variables ***must*** be set.

* `monero_pool_url` - The url to your monero pool.
* `monero_pool_username` - The username you use to log into your monero pool.
* `monero_pool_password` - The password for that username.
* `monero_donate_level` - The level to donate back to the xmrig devs.

For more information on those settings please see the xmrig documentation: https://github.com/xmrig/xmrig#usage.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      vars:
        xmrig_pool_url: stratum+tcp://mine.xmrpool.net:5555
        xmrig_pool_username: somemoneroaddress
        xmrig_pool_password: x
        xmrig_donate_level: 2
      roles:
         - mkell43.docker-xmrig-miner

License
-------

MIT

Additional Information
----------------------

Find out more about monero at https://getmonero.org/ and https://moneroworld.com/.

Don't Forget The Xmrig Devs...
------------------------------

Send them some donations for their hard work.

* XMR: `48edfHu7V9Z84YzzMa6fUueoELZ9ZRXq9VetWzYGzKt52XU5xvqgzYnDK9URnRoJMk1j8nLwEVsaSWJ4fhdUyZijBGUicoD`
* BTC: `1P7ujsXeX7GxQwHNnJsRMgAdNkFZmNVqJT`

Also... if you would like to send me a tip for this, I sure wouldn't mind.

* XMR - `4Adq5EZWCJ2jh4kttRSoa3KegN3K3KVnkZdATgd1XQcnZt7cJmggXHkjXqrT3anyZ22j7DEE74GkbVcQFyH2nNiC3c7HGvC`
* BTC - `3NDB2vgQEvje1qEYeGVLBWU5oqaGcFKq5D`
