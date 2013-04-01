## Description

This is a [logstash](http://logstash.net/) automated installation using [vagrant](http://www.vagrantup.com/) and the semi-official [logstash-cookbook](https://github.com/anthroprose/logstash-cookbook)

1. It use vagrant with the chef-solo provisioner. 
2. Manages chef cookbook dependancies using the excellent [Berkshelf](http://berkshelf.com) gem.
3. It uses the latest version of [Kibana](http://kibana.org) by using the latest [kibana cookbook](https://github.com/realityforge/chef-kibana).
4. An embedded version of [Elasticsearch](http://www.elasticsearch.org/) from within logstash.
5. It uses the logstash input for twitter stream api and looks for the following hash tags #aws, #cloud, #ec2, #CloudComputing, #devops, #openstack and #cloudstack.


## Install

Type the code below in terminal.

	$ git clone git://github.com/hatimabdalla/logstash-vagrant.git logstash-vagrant
	$ cd logstash-vagrant

Accept the .rvmrc file creation, then continue.

	$ bundle install
	$ berks install

Install the vagrant plugin berkshelf-vagrant as follows:

	$ vagrant plugin install berkshelf-vagrant

Update Vagrantfile with the twitter username and password.

	$ vagrant up

To access the Kibana web interface just browse to http://localhost:8080

## License
(The MIT License)

Copyright © 2009-2013 Hatim Abdalla

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the Software), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
