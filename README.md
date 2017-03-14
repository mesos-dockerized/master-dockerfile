# Mesos Master docker image

[![Build Status](https://travis-ci.org/mesos-dockerized/master-dockerfile.svg?branch=master)](https://travis-ci.org/mesos-dockerized/master-dockerfile) [![Docker Repository on Quay](https://quay.io/repository/mesosdockerized/mesos-master/status "Docker Repository on Quay")](https://quay.io/repository/mesosdockerized/mesos-master)

## Example usage
```
docker run -d --net=host --name=mesos-master \
 -e MESOS_ZK=zk://{EXTERNAL_IP}:2181/mesos \
 -e MESOS_QUORUM=1 \
 -e MESOS_REGISTRY=in_memory \
 -e MESOS_NO_HOSTNAME_LOOKUP=true \
 -e MESOS_IP={EXTERNAL_IP} \
 -e MESOS_LOG_DIR=/var/log/mesos \
 -e MESOS_WORK_DIR=/var/tmp/mesos \ 
 quay.io/mesosdockerized/mesos-master:v1.1.0
```

Check more examples in [mesos-dockerized/mesos-cluster][mesos-cluster-repo] repository.

[mesos-cluster-repo]: https://github.com/mesos-dockerized/mesos-cluster
