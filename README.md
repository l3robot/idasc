Image DataSet Creator
=====================

This project aggregates every image it can find based on a keyword search among
multiple data sources such as google images, bing images, picasa, flickr, etc.

Features
--------

* Can create datasets for research purposes in matter of minutes
* Easy to add backends
* Automatically prune duplicates (currently being developed)


Installation
------------

Please ensure that Python 3 is installed before proceeding. We highly
recommend using a virtual environment (which can be installed using 
`pip install virtualenv`).

    git clone https://github.com/soravux/idasc.git
    cd idasc
    virtualenv venv
    source venv/bin/activate
    pip install -r requirements.txt
    cp config.ini.dist config.ini
    nano config.ini


Getting keys
------------

* Bing: http://www.bing.com/dev/en-us/dev-center
* imgur: https://imgur.com/account/settings/apps
* flickr: https://www.flickr.com/services/apps/create/


Usage
-----

    python idasc.py [keyword]
    python idasc.py --help


### Adding a backend ###

Just create a new python module in the `backends` directory containing a
`go(keyword, path)` function. This function will receive the keyword entered
by the user and the path where it should download its images. Most backends are
similar and thus could be copied over another similar backend and modified. 

