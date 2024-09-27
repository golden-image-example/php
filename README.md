# php

```
podman build -f 8.2-fpm/Containerfile .
```

```
$ oc get route/quay-registry-quay -n quay-enterprise
NAME                               HOST/PORT                                                                                          PATH   SERVICES                           PORT   TERMINATION     WILDCARD
quay-registry-quay                 quay-registry-quay-quay-enterprise.apps.cluster-qgvvj.qgvvj.sandbox774.opentlc.com                        quay-registry-quay-app             http   edge/Redirect   None
```
podman pull quay-registry-quay-quay-enterprise.apps.cluster-qgvvj.qgvvj.sandbox774.opentlc.com/golden-image-example/nginx
docker pull quay-registry-quay-quay-enterprise.apps.cluster-qgvvj.qgvvj.sandbox774.opentlc.com/golden-image-example/nginx

podman pull quay-registry-quay-quay-enterprise.apps.cluster-qgvvj.qgvvj.sandbox774.opentlc.com/golden-image-example/php
docker pull quay-registry-quay-quay-enterprise.apps.cluster-qgvvj.qgvvj.sandbox774.opentlc.com/golden-image-example/php

```
oc new-project golden-image-example | oc project golden-image-example
oc create -f ./tekton/pipeline.yaml -n golden-image-example
```