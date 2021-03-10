# polling-helm
the helm chart package of polling app server

备注：

版本0.2.0为 Helm模版语言的简单版应用，没有应用_helpers.tpl，values.yaml只有简单内容

版本0.3.0为 Helm模版语言的轻量版应用，轻量应用_helpers.tpl，values.yaml有轻量内容

Helm模版语言的重量版应用，查看Helm Chart: auro_demo/polling，版本0.1.0，重量应用_helpers.tpl，values.yaml

部署命令：

helm repo update

helm fetch auro_demo/polling-server

helm fetch auro_demo/polling-server --insecure-skip-tls-verify（如果需要跳过tls验证）

tar -xzvf polling-server-0.2.0.tgz

cd polling-server

helm upgrade --install polling-server . -n demo