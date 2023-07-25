
## install amazon-ec2-net-utils

### Info

https://github.com/amazonlinux/amazon-ec2-net-utils

### Centos 7

#### 1.x版本

```bash
sudo su -

yum -y install git make systemd systemd-units rpm-build
git clone --branch=1.x --single-branch --depth 1 https://github.com/aws/amazon-ec2-net-utils.git
cd amazon-ec2-net-utils/
curl -LO 'https://github.com/aws/amazon-ec2-net-utils/archive/1.7.3.tar.gz'
rpmbuild --define "_sourcedir $PWD" -bb amazon-ec2-net-utils.spec
ls ~/rpmbuild/RPMS/noarch/
yum localinstall ls ~/rpmbuild/RPMS/noarch/amazon-ec2-net-utils-1.7.3-1.el7.noarch.rpm
```

```bash
yum -y install git make systemd systemd-units rpm-build &&\
git clone --branch=1.x --single-branch --depth 1 https://github.com/aws/amazon-ec2-net-utils.git &&\
cd amazon-ec2-net-utils/ &&\
curl -LO 'https://github.com/aws/amazon-ec2-net-utils/archive/1.7.3.tar.gz' &&\
rpmbuild --define "_sourcedir $PWD" -bb amazon-ec2-net-utils.spec &&\
ls ~/rpmbuild/RPMS/noarch/ &&\
yum localinstall ls ~/rpmbuild/RPMS/noarch/amazon-ec2-net-utils-1.7.3-1.el7.noarch.rpm
```

### Ubuntu/debian

https://tracker.debian.org/pkg/amazon-ec2-net-utils

https://launchpad.net/ubuntu/+source/amazon-ec2-net-utils

```bash
sudo su -
apt install dpkg-dev -y &&\
cd /tmp &&\
wget https://launchpad.net/ubuntu/+archive/primary/+files/amazon-ec2-net-utils_2.3.0-3_all.deb &&\
chmod a+rwx amazon-ec2-net-utils_2.3.0-3_all.deb  &&\
apt install ./amazon-ec2-net-utils_2.3.0-3_all.deb 
```