---
tags:
  - links
  - k8s
  - courses
title: Kubernetes
share: "true"
---
# Ссылки и полезные ресурсы по Kubernetes
Как тренироватьcя: Minikube, на Mac и Windows — Rancher Desktop.
vSAN datastore can only upload VMDK files using the VMware stream optimized format.
[GetAmbassador](https://www.getambassador.io/editions) —облако Kubernetes c Emissary, telepresence. ArgoCD, Envoy.
[Emissary](https://www.getambassador.io/docs/emissary/latest/tutorials/getting-started) Ingress (альтернатива Istio), [Github](https://github.com/emissary-ingress/emissary)
[Shipmight](https://shipmight.com/) is a Developer Platform which runs on any Kubernetes cluster. Think Heroku, but on  your infrastructure.
[ArgoCD, Helm Charts, and Garden](https://garden.io/blog/argo-cd-helm-charts): A winning GitOps combination for CI/CD
[k8s-bench-suite](https://github.com/InfraBuilder/k8s-bench-suite) — тестировать кластер Kubernetes. Важно при создании кластеров. Мы тестируем сеть Cilium. Скрипт от Cilium на go не подходит, там hardcode внутри на image и прочее.
[Kubescape](https://www.armosec.io/kubescape/#) — An **open-source** Kubernetes security platform for your IDE, CI/CD pipelines, and clusters. Kubescape is one of the fastest-growing Kubernetes security and compliance open source projects. Targeted at the DevSecOps practitioner or platform engineer, it includes risk analysis, security compliance, and misconfiguration scanning. It offers an easy-to-use CLI interface, flexible output formats, and much more. Bottom line, Kubescape saves Kubernetes users and admins precious time, effort, and resources.
[Сертификация](https://sbulav.github.io/certifications/passed-few-free-kubernetes-certifications/) по calico, kyverno.
[Kyverno](https://kyverno.io/) — Kubernetes Native Policy Management
[Giant Swarm](https://www.giantswarm.io/) offers a fully managed, open-source Cloud Native Developer Platform with all the flexibility and support you need.
https://www.notion.so/Start-Kubernetes-Live-bc3c8afec6f64731aa2ebcec264efcfa — лайвстримы и слайды
[Robusta](https://home.robusta.dev/) — Kubernetes Monitoring. Best practices built-in. We built an open-source observability engine and combined it with Prometheus monitoring. Setup monitoring and alerting in minutes with a single helm install. Default alerts included.
[Elastisys Compliant Kubernetes](https://elastisys.io/compliantkubernetes/) — готовая система кубера и всякого разного, но платная. Просто для примера.
[Jiju](https://juju.is/) — open source orchestration engine for software operators that enables the deployment, integration and lifecycle management of applications at any scale, on any infrastructure using charms. A charm is an operator - business logic encapsulated in reusable software packages that automate every aspect of an application's life.
[Sloop](https://github.com/salesforce/sloop) — Kubernetes history visualization.

Что интересного появилось за месяц в [Kubernetes this month](https://www.youtube.com/playlist?list=PLI1_CQcV71RnSeiizLChZXNz27nemT0sy), Nigel Poulton. Или у него на [канале](https://www.youtube.com/watch?v=06EW2sOeavo&list=PLJ7W8yyb6PiwpmWmL58lxqHtvTf1vYjJK&pp=iAQB).
https://codeutility.org — много разборов ошибок
[Уроки по Kubernetes](https://www.youtube.com/playlist?list=PL3SzV1_k2H1VDePbSWUqERqlBXIk02wCQ) на русском
Курс по Kubernetes на английском, крутой YouTube канал [Just me and Opensource](https://www.youtube.com/playlist?list=PL34sAs7_26wNBRWM6BDhnonoA5FMERax0)
Канал [That DevOps Guy](https://www.youtube.com/@MarcelDempers)
[Learn Kubernetes with Civo Academy](https://www.civo.com/academy)
[Kubernetes 101 Series' Articles](https://dev.to/leandronsp/series/21979)
[Killercoda](https://killercoda.com/) is a place where you open your browser and get instant access to a real Linux or Kubernetes environment ready to use. These environments are maintained remotely and accessed locally, hence no setup or huge resource usage in local browsers. As a user you can learn from existing scenarios and as a creator you can provide scenarios to teach any kind of tools or technologies.
[Kube by Example](https://kubebyexample.com/en/learning-paths) We're here to offer you the resources, tools, and know-how to develop Kubernetes and related cloud-native skills with learning paths that range from beginner to advance levels.
[KubeSphere](https://kubesphere.io/projects/) is committed to the open source contribution of cloud native technology, enriching the ecosystem of the open source community.

[Advanced Kubernetes YAML configurations & templates](https://github.com/HariSekhon/Kubernetes-configs) — лучшие практики настроек манифестов для Kubernetes. The top-level directory contains standard Kubernetes object templates with many Best Practices, Tips & Tricks learned over time across production environments. The sub-directories contain ready-to-run real world apps that I've run across environments.


[k'exp](https://github.com/iximiuz/kexp) — Kubernetes Explorer. Understand Kubernetes — the visual way. Not yet another attempt to manage production clusters in the browser. k'exp can reflect the state of your cluster in real-time. k'exp is for:
- Learning and exploring Kubernetes capabilities
- Application development (object graph _presets_ for every app)
- Controller and operator development (dynamic object graphs)
- [coming soon] Postman-like client and request builder for Kubernetes API
Софт поможет разобраться в Kubernetes через визуализацию. kexp предназначен для:
• изучения возможностей Kubernetes
• разработки приложений
• разработки контроллера и оператора

Установка последней версии с GitHub:
```sh
GOOS=linux
GOARCH=amd64
curl -Ls https://github.com/iximiuz/kexp/releases/latest/download/kexp_${GOOS}_${GOARCH}.tar.gz | tar xvz
sudo mv kexp /usr/local/bin
```

Использование
Это статически связанный двоичный файл Go со встроенным UI. Если у вас уже настроен kubectl для доступа к вашим кластерам, вы также можете запустить kexp — он использует ту же логику обнаружения KUBECONFIG.
По умолчанию kexp запускает сервер на localhost:5173:
```sh
kexp
open localhost:5173
```
В качестве альтернативы вы можете указать кастомный адрес:
```sh
kexp --host 0.0.0.0 --port 8090
```

## Деплой в Kubernetes
- деплой только через Helm чарты, автоматизированный через GitLab CI
- [Flux](https://github.com/weaveworks/flux)
- [Argo CD](https://argoproj.github.io/argo-cd/)
- [Razee](https://razee.io)
- [Fleet](https://fleet.rancher.io/)

Можно взять k3s или k0s, добавить kubevirt и это в огромном подавляющем числе упростит и первоначальную настройку и расширит рабочие нагрузки. А в случае роста узлов и подов, можно делать мультикластерные решения и это в любом случае потребует затрат специалистов для обслуживания инфраструктуры. Сейчас нет никаких преимуществ в новых проектах использовать что-то отличное от k8s.
База данных в Кубернетес.k3s отличается разве что тем, что там все упаковано в один бинарник — coredns, local path provisioner, api server, metrics server, nginx, etcd и все остальное. Т.е. сложность системы никак не меняется. При этом за счет того, что проект это все таки другой, глюков своих у них хватает. Мы k3s пробовали, наелись всякой ерунды с ним (чето вроде с конфигами по дефолту была фигня, что нельзя было перенастроить все эти встроенные компоненты. etcd не работал), что подумали ну его нафиг. Лучше кубспреем разольем ванильный кубер. Теже яйца только в профиль

```bash
git clone -b rebrain-event https://github.com/percona/percona-xtradb-cluster-operator.git
```

## backstage
Как упростить и улучшить жизнь разработчиков в инфраструктурах с Kubernetes (да и не только).

Кто-то может тут сразу поднять вопрос: "Нужно ли разработчику знать Kubernetes?" - об этом у меня был отдельный пост (https://t.me/k8security/213) и в рамках нее упоминается статья "Maximizing Developer Effectiveness (https://martinfowler.com/articles/developer-effectiveness.html)". Из которой вы и могли уже узнать о таком замечательном проекте от команды Spotify как Backstage (https://backstage.io/).

[Backstage](https://github.com/backstage/backstage) — OpenSource портал для разработчиков с системой [плагинов](https://backstage.io/plugins), позволяющий обозревать всю информацию о системе в одном месте! И да эта система уже понимает, что такое [Kubernetes](https://backstage.io/blog/2021/01/12/new-backstage-feature-kubernetes-for-service-owners) !

Проект находится в [CNCF Sandbox](https://www.cncf.io/projects/backstage/), у него более [50](https://backstage.io/blog/2021/09/30/50-public-adopters) крупных публичных компаний пользователей. Я знаю и российские компании, которые используют данное решение.

Прямо online можно поиграть с решением на данном [demo](https://demo.backstage.io/) стенде.

## Ссылки
Kubernetes [README](https://kubereadme.com/) ([Github](https://github.com/chris-short/kubernetesreadme.com)).
[KubeCon + CloudNativeCon Europe 2021](https://www.youtube.com/watch?v=2cW8_h98sn8&list=PLj6h78yzYM2MqBm19mRz9SYLsw4kfQBrC) — видео с конференции
Deploy [Kubernetes in Kubernetes](https://github.com/kvaps/kubernetes-in-kubernetes) using Helm
[arkade](https://github.com/alexellis/arkade) — The Open Source Kubernetes Marketplace
[Paralus](https://www.paralus.io/) — управление доступом Kubernetes (RBAC, OIDC) с веб-интерфейсом.
[DevSpace](https://www.devspace.sh/) — open-source developer tool for Kubernetes that lets you develop and deploy cloud-native software faster.
https://github.com/diegolnasc/kubernetes-best-practices
https://www.golinuxcloud.com/kubernetes-tutorial/
[Kubernetes The Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way) — изучение того что под капотом kubernetes.
[Kube Academy](https://kube.academy/courses) — бесплатные курсы от VMWare
https://github.com/lucassha/CKAD-resources — ресурсы для подготовки к экзамену
https://github.com/k8s-at-home/ — Kubernetes at home. https://k8s-at-home.com/ Всё для изучения дома. И helm.  [Discord](https://discord.gg/sTMX7Vh)
https://acloud.guru/series/kubernetes-this-month — что обновилось в Kubernetes, ежемесячный обзор.
https://vvv.space/kubernetes — ссылки по Kubernetes
https://killer.sh/ — подготовиться перед экзаменом Kubernetes
https://github.com/terrytangyuan/awesome-argo — ресурсы и проекты по **ArgoCD**
https://editor.cilium.io/ — обучение, как создавать Networking Policy для Kubernetes. makes it easy to build, visualize, and make sense of Network Policies, which can then be downloaded as YAML and run in any Kubernetes cluster with a Network Policy-aware CNI.
https://orca.tufin.io/netpol/ — Kubernetes Network Policy Viewer. The Tufin Kubernetes Policy Viewer is a visualization tool for cluster admins to make Kubernetes network policy definitions intuitive and understandable. Just copy/paste your YAML code or upload a YAML file and click for an instant visual representation of your policy with a deta.
https://github.com/itaysk/kubectl-neat —  Clean up Kuberntes yaml and json output. Clean up Kuberntes yaml and json output to make it readable
https://github.com/2gis/k8s-handle — Easy CI/CD for Kubernetes clusters with python and jinja2 - 2gis/k8s-handle
https://ingressbuilder.jetstack.io/ — [Ingresses](https://kubernetes.io/docs/concepts/services-networking/ingress/ "Kubernetes Ingress") are Kubernetes resources used to direct HTTP and HTTPS traffic to your cluster services. In order to correctly use an ingress resource a dedicated [ingress-controller](https://kubernetes.io/docs/concepts/services-networking/ingress-controllers/ "Kubernetes Ingress Controllers") must be present and running in the host cluster. Ingress Builder allows users to select any annotation from the list of available controllers, to add to the ingress manifest.

Хранение секретов:
[Hashicorp Vault](https://learn.hashicorp.com/vault)
[AppRole](https://developer.hashicorp.com/vault/docs/auth/approle) для авторизации на виртуальных машинах.
[Manage Kubernetes secrets with Mozilla SOPS](https://fluxcd.io/flux/guides/mozilla-sops/).
[HashiCorp Vault перехвален, а Mozilla SOPS вместе с KMS и Git неоправданно недооценены](https://habr.com/ru/company/nixys/blog/572102/)
[Protecting Ansible secrets with Mozilla SOPS](https://docs.ansible.com/ansible/latest/collections/community/sops/docsite/guide.html)

https://reconshell.com/best-kubernetes-tools-for-managing-devops-projects/
[kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters](https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/)

Storage:
- [Kadalu](https://github.com/kadalu/kadalu/tree/devel) is a project to provide Persistent Storage in container ecosystem (like kubernetes, openshift, RKE, etc etc). Kadalu operator deploys CSI pods, and **gluster storage** pods as per the config. You would get your PVs served through APIs implemented in CSI.
- [Kubernetes Data Mobility with Cloud Volumes ONTAP](https://cloud.netapp.com/blog/cvo-blg-kubernetes-data-mobility-with-cloud-volumes-ontap)
- [Scaling Kubernetes Persistent Volumes with Cloud Volumes ONTAP](https://cloud.netapp.com/blog/cvo-blg-scaling-kubernetes-persistent-volumes-with-cloud-volumes-ontap)
- [What's New in K8S 1.23?](https://cloud.netapp.com/blog/cvo-blg-whats-new-in-k8s-1.23)
- [Kubernetes Topology-Aware Volumes and How to Set Them Up](https://cloud.netapp.com/blog/cvo-blg-kubernetes-topology-aware-volumes-and-how-to-set-them-up)
- [How to Use NetApp Cloud Manager for Provisioning Persistent Volumes in Kubernetes](https://cloud.netapp.com/blog/using-cloud-manager-for-kubernetes-deployment)
- [Kubernetes vs. Nomad: Understanding the Tradeoffs](https://cloud.netapp.com/blog/cvo-blg-kubernetes-vs-nomad-understanding-the-tradeoffs)
- [How to Set Up MySQL Kubernetes Deployments with Cloud Volumes ONTAP](https://cloud.netapp.com/blog/how-to-set-up-mysql-kubernetes-deployments)
- [Kubernetes Volume Cloning with Cloud Volumes ONTAP](https://cloud.netapp.com/blog/kubernetes-persistent-volumes-cloning)
- [Container Storage Interface: The Foundation of K8s Storage](https://cloud.netapp.com/blog/cvo-blg-container-storage-interface-the-foundation-of-k8s-storage)
- [Kubernetes Deployment vs StatefulSet: Which is Right for You?](https://cloud.netapp.com/blog/cvo-blg-kubernetes-deployment-vs-statefulset-which-is-right-for-you)
- [Kubernetes for Developers: Overview, Insights, and Tips](https://cloud.netapp.com/blog/kubernetes-for-developers-a-deep-dive)
- [Kubernetes StatefulSet: A Practical Guide](https://cloud.netapp.com/blog/cvo-blg-kubernetes-statefulset-a-practical-guide)
- [Kubernetes CSI: Basics of CSI Volumes and How to Build a CSI Driver](https://cloud.netapp.com/blog/cvo-blg-kubernetes-csi-basics-of-csi-volumes-and-how-to-build-a-csi-driver)
- [Kubernetes Management and Orchestration Services: An Interview with Michael Shaul](https://cloud.netapp.com/blog/cvo-blg-a-closer-look-at-kubernetes-management-orchestration-services)
- [Kubernetes Database: How to Deploy and Manage Databases on Kubernetes](https://cloud.netapp.com/blog/cvo-blg-kubernetes-database-how-to-deploy-manage-dbs-on-kubernetes)
- [Kubernetes and Persistent Apps: An Interview with Michael Shaul](https://cloud.netapp.com/blog/cvo-blg-kubernetes-and-persistent-apps-an-interview-with-michael-shaul)
- [Kubernetes: Dynamic Provisioning with Cloud Volumes ONTAP and Astra Trident](https://cloud.netapp.com/blog/dynamic-kubernetes-persistent-volume-provisioning)
- [Kubernetes Cloud Storage Efficiency with Cloud Volumes ONTAP](https://cloud.netapp.com/blog/storage-efficiency-for-improving-persistent-volume-storage-costs)
- [Data Protection for Persistent Data Storage in Kubernetes Workloads](https://cloud.netapp.com/blog/protection-for-persistent-data-storage-in-kubernetes)
- [Managing Stateful Applications in Kubernetes](https://cloud.netapp.com/blog/managing-stateful-applications-in-kubernetes)
- [Kubernetes: Provisioning Persistent Volumes](https://cloud.netapp.com/blog/understanding-kubernetes-persistent-volume-provisioning)
- [An Introduction to Kubernetes](https://cloud.netapp.com/blog/an-introduction-to-kubernetes)
- [Google Kubernetes Engine: Ultimate Quick Start Guide](https://cloud.netapp.com/blog/gcp-cvo-blg-google-kubernetes-engine-ultimate-quick-start-guide)
- [Kubernetes Persistent Volumes, Claims, Storage Classes, and More](https://cloud.netapp.com/blog/kubernetes-persistent-storage-why-where-and-how)
- [Azure Kubernetes Service Tutorial: How to Integrate AKS with Azure Container Instances](https://cloud.netapp.com/blog/azure-cvo-blg-azure-kubernetes-service-tutorial-integrate-aks-with-aci)
- [Kubernetes Workloads with Cloud Volumes ONTAP: Success Stories](https://cloud.netapp.com/blog/cvo-blg-kubernetes-workloads-with-cloud-volumes-ontap-success-stories)
- [Container Management in the Cloud Age: New Insights from 451 Research](https://cloud.netapp.com/blog/cvo-blg-container-management-in-the-cloud-age-new-insights-from-451-research)
- [Kubernetes Storage: An In-Depth Look](https://cloud.netapp.com/blog/cvo-blg-kubernetes-storage-an-in-depth-look)
- [Monolith vs. Microservices: How Are You Running Your Applications?](https://cloud.netapp.com/blog/cvo-blg-monolith-vs.-microservices-how-do-you-run-your-applications)
- [Kubernetes Shared Storage: The Basics and a Quick Tutorial](https://cloud.netapp.com/blog/kubernetes-shared-storage-the-basics-and-a-quick-tutorial)
- [Kubernetes NFS Provisioning with Cloud Volumes ONTAP and Trident](https://cloud.netapp.com/blog/how-to-provision-kubernetes-persistent-volumes-for-nfs-services)
- [Azure Kubernetes Service How-To: Configure Persistent Volumes for Containers in AKS](https://cloud.netapp.com/blog/azure-cvo-blg-azure-kubernetes-service-configuring-persistent-volumes-in-aks)
- [Kubernetes NFS: Quick Tutorials](https://cloud.netapp.com/blog/kubernetes-nfs-two-quick-tutorials-cvo-blg)
- [NetApp Trident and Docker Volume Tutorial](https://cloud.netapp.com/blog/docker-volume-tutorial-using-trident-to-provision-storage)