# this files describes how to build tsuru go image
# to run it:
# 1- install docker
# 2- run $ docker build -t tsuru/go https://raw.github.com/tsuru/basebuilder/master/go/Dockerfile

from	base:ubuntu-quantal
run	apt-get install wget -y --force-yes
run	wget http://github.com/tsuru/basebuilder/tarball/master -O basebuilder.tar.gz --no-check-certificate
run	mkdir /var/lib/tsuru
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	cp /var/lib/tsuru/go/deploy /var/lib/tsuru
run	cp /var/lib/tsuru/install /var/lib/tsuru
run	cp /var/lib/tsuru/start /var/lib/tsuru
run	cp /var/lib/tsuru/stop /var/lib/tsuru
run	/var/lib/tsuru/go/install
run	/var/lib/tsuru/base/setup
