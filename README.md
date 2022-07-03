# traininng_task
Training task with Ansible + k8s

## Задание: Развернуть с помощью ansible роли minikube, в котором задеплоить образ "hello world" с балансировщиком ingress-nginx, используя https.

Среда контейнеризации: Docker

Среда оркестрации: minikube

Операционная система: Ubuntu 20.04 (для CentOS 7/8 не получилось проверить)

Балансировщик: Nginx

Образ hello-world: gcr.io/google-samples/hello-app:1.0

Необходимо написать ansible роль, которая автоматически установит minukube и развернет там nginx с https(ssl) в качестве балансировщика для приложения hello world. Сертификат можно использовать любой(letsencrypt, самоподписанный), количество реплик приложения 3. Также настроить в конфигурации приложения hello-world доступность 100% подов при обновлении.

### Запуск
Предполагается, что на хостовой машине настроен Ansible.

    ansible-playbook all.yml -K
