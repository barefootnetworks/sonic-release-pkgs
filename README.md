# sonic-release-pkgs

Upgrade SDE on SONiC

Copy SDE Debian packages into SONiC environment

scp bfnsdk_1.0.0_amd64.deb admin@<switchip>:/home/admin/
scp bfnplatform_1.0.0_amd64.deb admin@<switchip>:/home/admin/

Copy SDE Debian packages into SONiC syncd Docker container

ssh admin@<switchip>
docker cp bfnsdk_1.0.0_amd64.deb syncd:/opt/bfn/
docker cp bfnplatform_1.0.0_amd64.deb syncd:/opt/bfn/
Install SDE Debian packages

docker exec -ti syncd bash
cd /opt/bfn/
dpkg -i bfnsdk_1.0.0_amd64.deb
dpkg -i bfnplatform_1.0.0_amd64.deb
