# sonic-release-pkgs
Upgrade SDE on SONiC

Copy SDE Debian packages into SONiC environment

scp bfnsdk_rt_202007_deb9.deb admin@switchip:/home/admin/

scp bfnplatform_rt_202007_deb9.deb admin@switchip:/home/admin/

Copy SDE Debian packages into SONiC syncd Docker container

ssh admin@switchip

docker cp bfnsdk_rt_202007_deb9.deb syncd:/opt/bfn/

docker cp bfnplatform_rt_202007_deb9.deb syncd:/opt/bfn/

Install SDE Debian packages

docker exec -ti syncd bash

cd /opt/bfn/

dpkg -i bfnsdk_rt_202007_deb9.deb

dpkg -i bfnplatform_rt_202007_deb9.deb
