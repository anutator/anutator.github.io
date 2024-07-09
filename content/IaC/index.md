---
title: IaC
share: "true"
---
## Terraform
[OpenTofu](https://opentofu.org/) — форк Terraform, его бесплатная полностью OpenSource альтернатива
[Terraform Best Practices](https://github.com/ozbillwang/terraform-best-practices)
[Introducing Infrastructure Manager: Provision Google Cloud resources with HashiCorp Terraform](https://cloud.google.com/blog/products/management-tools/introducing-infrastructure-manager-powered-by-terraform)

## AWS
You read the documentation.
So for AWS stuff, anything you want to do you can do using the [boto3 lib](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
AWS CDK is also well documented, but I also suggest googling how others have done things as examples are always handy.
[https://docs.aws.amazon.com/cdk/api/v2/python/](https://docs.aws.amazon.com/cdk/api/v2/python/)
For the last one Serverless is super well documented on doing the exact task I recommended. You just have to work out how to write the lambda. Zero-Friction
Serverless Apps on AWS Lambda: [https://www.serverless.com/framework/docs/providers/aws/events/apigateway](https://www.serverless.com/framework/docs/providers/aws/events/apigateway)
This all requires some AWS experience. If you're not familiar I'm happy to give you some similar examples for other cloud providers. Or I can suggest something that's just local but that you can follow any old learn python thing for.

## Ansible
[Acsender](https://github.com/ctrliq/ascender) — веб-интерфейс управления инфраструктурой через Ansible. Ascender provides a web-based user interface, REST API, and task engine built on top of [Ansible](https://github.com/ansible/ansible). It is based off the upstream project of [AWX](https://github.com/ansible/awx). Посмотреть другие [продукты](https://ciq.com/), в том числе [Warewulf](https://ciq.com/products/warewulf/) — whether you’re managing tens of nodes or tens of thousands, you want the simplest way to provision the operating system, a single point of control, and ease of configuration.
[Ansible Tower Workshop on Azure](http://redhatgov.io/workshops/ansible_tower_azure/) — пройти эти workshop-ы в видеоуроках
[Ansible Tutorial](https://github.com/leucos/ansible-tuto/)
[Лабораторные работы по курсам](https://github.com/bykvaadm/OS/tree/master#лабораторные-работы-по-курсам) на русском, в том числе Ansible.
[Вебинары и тренинги](https://www.ansible.com/resources/webinars-training)
[Бесплатные курсы и руководства](https://hackr.io/tutorials/learn-ansible?fbclid=IwAR3fcxaMv6iY3ldEGhcncqhLGe6dlLs0s-TVhhMH7BMKUu4n8L2oZsU6aEQ)
Полезности — [Learn Delivery](https://github.com/lean-delivery). Проверка правописания, примеры ролей для баз данных.
[https://www.thecloud.coach/ansible-crash-course](https://www.thecloud.coach/ansible-crash-course) — курс!
[Плагин](https://plugins.jetbrains.com/plugin/14893-ansible/versions) — для IntelliJ IDEA (Jetbrains).
[pdsh](https://github.com/chaos/pdsh) — параллельное выполнение команд в кластере, на нескольких серверах. Некий аналог Ansible для простых команд.
Роль настройки файрвола [ufw](https://github.com/Oefenweb/ansible-ufw) в Debian
[ARA](https://ara.recordsansible.org/) Records Ansible and makes it easier to understand and troubleshoot. ARA provides Ansible reporting by recording `ansible` and `ansible-playbook` commands regardless of how and where they run.

https://stackoverflow.com/questions/25977410/adding-an-fstab-option-using-ansible  проверка */etc/fstab*
https://gitlab.com/deusops/lessons/
https://gitlab.com/devops_influence/otus/ansible-nginx
https://gitlab.com/devops_influence/ansible-roles

```
 .cicd
├── docker
│   ├── docker-compose.yml
│   └── Dockerfile
├── docker-compose.yml
├── inventories
│   └── dev
│       └── hosts
├── playbook.yml
└── requirements.yml
```

Top 7 Ansible articles from 2018
1. [How to use Ansible to patch systems and install applications](https://opensource.com/article/18/3/ansible-patch-systems) Learn how to save time doing updates with the Ansible IT automation engine.
2. [A sysadmin's guide to Ansible: How to simplify tasks](https://opensource.com/article/18/7/sysadmin-tasks-ansible) There are many ways to automate common sysadmin tasks with Ansible. Here are several of them.
3. [How to manage your workstation configuration with Ansible](https://opensource.com/article/18/3/manage-workstation-ansible) Learn how to automate your workstation setup via Ansible, which will allow you to easily restore...
4. [How to use Ansible to set up system monitoring with Prometheus](https://opensource.com/article/18/3/how-use-ansible-set-system-monitoring-prometheus) In the third part of this Ansible how-to series, learn how to automate system monitoring.
5. [An introduction to Ansible Operators in Kubernetes](https://opensource.com/article/18/10/ansible-operators-kubernetes) The new Operator SDK makes it easy to create a Kubernetes controller to deploy and manage a service or application in a cluster.
6. [4 Ansible playbooks you should try](https://opensource.com/article/18/8/ansible-playbooks-you-should-try) Streamline and tighten automation processes in complex IT environments with these Ansible playbooks.
7. [Manage your workstation with Ansible: Automating configuration](https://opensource.com/article/18/3/manage-your-workstation-configuration-ansible-part-2)