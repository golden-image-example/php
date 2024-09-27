# php

```
podman build -f 8.2-fpm/Containerfile .
```

```
oc new-project golden-image-example | oc project golden-image-example
oc create -f ./tekton/pipeline.yaml -n golden-image-example
```