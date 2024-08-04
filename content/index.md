---
share: "true"
title: О сайте
---
Если нажать на название раздела, появится общая информация по разделу (если я создавала такое описание) либо список статей раздела.

Материал в разделах:
**Gitlab** — всё что касается работы с кодом: техники работы с git, работа и пайплайны в Gitlab (рассматривается только бесплатный вариант Gitlab), Gitlab-раннеры, Github Actions.
**IaC** (инфраструктура как код) — всё, что касается автоматизации разворачивания и настройки инфраструктуры: [Ansible](https://docs.ansible.com/ansible-core/2.16/index.html), [Terraform](https://www.terraform.io/), [OpenTofu](https://opentofu.org/) (форк Terraform), [Atlantis](https://www.runatlantis.io/), [Terragrunt](https://terragrunt.gruntwork.io/).
**Docker** — контейнеры, не только docker, но и containerd, podman. Сборка через dind, kaniko, buildah. Хранение контейнеров в Gitlab, Harbor.
**Telecom** — статьи по предыдущей работе (телефония, контактные центры Avaya, CISCO, Asterisk) и сетям.
**Kubernetes** — всё что связано с Kubernetes, Helm чартами, ArgoCD.
**Databases** — базы данных SQL, NoSQL, брокеры (Kafka, RabbitMQ, ActiveMQ).
**Linux** — темы по Linux, bash.
**DevOps** — всё что касается DevOps, но не вошло в другие разделы. Включает раздел web (Nginx, Apache, HAProxy).

Разделы могут содержать смежные темы, например роль Kubespray разворачивает Kubernetes, но возможны заметки по ней в разделе Ansible. Docker может содержать информацию по сборке в Gitlab. Введу теги, которые помогут соотносить статью с несколькими темами.

## Импортозамещение
Замена для управление заявкам и проектами Jira:
- [GLPI](https://www.glpi-project.org/) — Information Resource-Manager with an additional Administration Interface. Как выяcнилось, прилично ограничений в бесплатной версии. Писать плагины на php.
- [Taiga](https://taiga.io/) — free and open-source project management tool

Замена документирования, википедии Confluence:
- [BookStack](https://www.bookstackapp.com/) — на php, использовала.
- [Wiki.js](https://js.wiki/) — на node.js, ближе к Confluence (более навороченный).
- Если компания небольшая, достаточно будет встроенной в Gitlab [Wiki](https://docs.gitlab.com/ee/user/project/wiki/) и системы [заявок](https://docs.gitlab.com/ee/user/project/issues/) вместо Confluence+Jira.

Замена для виртуализации VMware:
- [XCP-ng](http://www.xcp-ng.org/) — Based on Citrix XenServer, XCP-ng is a fully open source virtualization platform. На неё многие переходят за рубежом.
- [OpenStack](https://www.openstack.org/) — очень сложно поддерживать.
- [Proxmox VE](https://www.proxmox.com/proxmox-ve) — для небольших компаний и домашней лабы.

Корпоративный чат и видеоконференции вместо Microsoft teams:
- [Zulip](https://zulip.com/) — похож на Slack, используют в одном банке точно. [Self-hosted](https://zulip.com/plans/#self-hosted) есть фактически весь [функционал](https://zulip.com/features/). Видеоконференцсвязь: по умолчанию интеграция с [Jitsi meet](https://jitsi.org/jitsi-meet/)  (для Kubernetes есть [k8s-jibri](https://github.com/itsmaniche18/jibri-kubernetes))
- [Matrix](https://matrix.org/). Разворачивание в контейнерах через [Ansible](https://github.com/spantaleev/matrix-docker-ansible-deploy), по умолчанию [Matrix Synapse](https://github.com/element-hq/synapse), поддерживает SSO. Synapse is an open source [Matrix](https://matrix.org) homeserver implementation, written and maintained by [Element](https://element.io). [Matrix](https://github.com/matrix-org) is the open standard for secure and interoperable real time communications. You can directly run and manage the source code in this repository, available under an AGPL license. There is no support provided from Element unless you have a subscription.
- [Rocket.chat](https://www.rocket.chat/) — уже не совсем бесплатный.
- [Nextcloud talk](https://nextcloud.com/blog/nextcloud-talk-open-source-online-video-conferencing-software/) — open-source video conferencing and chat application. Designed to keep all your online conversations private, whether by video or chat, all data is kept on your own servers and no data – not even metadata – can be leaked. [Github](https://github.com/nextcloud/spreed)

Пробовали Express.ms. Платный и глючил. ВКС пока через DION, но это внешний сервис и платный.

Операционная система Linux:
- российские тут не рассматриваю: RedOS с проблемами, AstraLinux — ну...
- [Rocky Linux](https://rockylinux.org/) вместо CentOS, RHEL, Oracle Linux.

Замена Microsoft Office:
[OnlyOffice](https://www.onlyoffice.com/ru/document-management.aspx) — бесплатные и платные версии.

Замена ElasticSearch:
- [VictoriaLogs](https://docs.victoriametrics.com/victorialogs/)
- [OpenSearch](https://opensearch.org/)