# Vagrant files

A base box based on centos7 with the virtualbox guest additions and docker.

The base box is published at jill-sato/centos7

## Build the base box

```bash
  cd base-box
  vagrant up
  VBoxManage list vms
  vagrant package --base vagrant-base-box_default_1543721538565_87996
```

To publish the box go to https://app.vagrantup.com/jill-sato/boxes/centos7

## Test the base box locally

```bash
  mkdir test-base-box
  vagrant box add centos7-custom ../base-box/package.box
  vagrant init centos7-custom
  vagrant up
```

## Create a vm with the base box

This will use the published base box.

```bash
  cd my-vm
  vagrant up
```
