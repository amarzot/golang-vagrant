# golang-vagrant
This project serves as a jumping off point for those looking to develop with vagrant and golang. Be sure to clone or download this repository to somewhere within your gopath. This ensures that the gopath the host and guest (vagrant) machines see is identical. By doing this, when developing in an IDE on the host computer it will see the same dependencies and be able to offer helpful code completion and error detection. At the same time, the guest machine will be able to compile it's own version of the source code and you get all the benefits of a shared development environment between coworkers.

### Prerequisites
* Vagrant
* Golang (although this isn't really necessary[\*](#gopath))

#### GOPATH
\* The Vagrantfile relies on the GOPATH environment variable existing. Installing Golang will set this environment variable for you, but you could, in theory, set it yourself. 

## Quick Setup
This guide should work on most platforms.

1. The first step is to clone or just download the repository to somewhere in your gopath.
```
cd C:\Users\Me\go\src\
git clone https://github.com/amarzot/golang-vagrant.git
```

2. Start and SSH into the Vagrant
```
vagrant up
...
vagrant ssh
```

3. Navigate to your project with in the Vagrant machine
```
cd /home/vagrant/go/src/golang-vagrant/
```

4. Build and run!
```
go build main.go
go run main.go
```
