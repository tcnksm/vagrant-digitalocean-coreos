Create CoreOS cluster on DigitalOcean by Vagrant [![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](https://github.com/tcnksm/vagrant-digitalocean-coreos/blob/master/LICENSE)
====

`Vagrantfile` and `cloud-config` to play with [CoreOS](https://coreos.com/) on DigitalOcean.

## Setup

To use this `Vagrantfile`, you need some setting.

### Environmental variables

You need to set below environmental variables:

```bash
export TOKEN="" 
export SSH_KEY_NAME=""
```

You can get `TOKEN` from DigitalOcean console (you should make it with read and write autority). `SSH_KEY_NAME` is your ssh-key registered in DigitalOcean.

### etcd token

And you need to generate new `etcd` token and write it in `user-data.yml`'s `etcd.service`:

```bash
$ curl -w "\n" https://discovery.etcd.io/new
```

### Vagrant-digitalocean plugin

Now (2014.11), [vagrant-digitalocean](https://github.com/smdahlen/vagrant-digitalocean) plugin is still 0.7 and we can't use `user-data` posting. But if you build it by yourself, you can use it.

```bash
$ git clone https://github.com/smdahlen/vagrant-digitalocean
$ gem build vagrant-digitalocean.gemspec
$ vagrant plugin install vagrant-digitalocean-0.7.0.gem 
```

## Usage

Decide how many cluste do you up:

```bash
$ export NUM_INSTANCES=3
```

And up it,

```bash
$ vagrant up --provider=digital_ocean
```

## Author

[tcnksm](https://github.com/tcnksm)


