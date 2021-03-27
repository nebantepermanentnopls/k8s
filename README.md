# Команды для k8s


```kubectl get pods``` - показать pods(deploy, nodes, hpa, rs) кластера;

```kubectl describe pods nginx``` -  описание pods(deploy, nodes..);

```kubectl port-forward nginx 9999:80``` - прокинуть порны с пода на хост;

```kubectl delete pods ``` - удалить;

```kubectl run name --image nginx --port 80``` - запуск контейнра;

```kubectl create deploy nginx --image nginx``` - создать deploy с контейнером nginx;

```kubectl scale deployment nginx --replicas 4``` - увеличить количество подов в деплоймнте;

```kubectl autoscale deploy nginx --min=4 --max=8 --cpu-percent=80``` - добавить автоскейл к деплою;

```kubectl rollout history deploy/nginx``` - история обновлений имеджа в деплое;

```kubectl rollout status deploy/nginx``` - история обновлений имеджа в деплое;

```kubectl set image deploy/nginx nginx=nginx:alpine --record``` - замена имеджа в деплое;

```kubectl rollout undo deploy/nginx --to=revision 1``` - откат к прошлой версии под номеров 1 в rollout history;

```kubectl rollout restart deploy/nginx``` - перекачать последнюю версию имеджа;

```kubectl apply -f deploy-create.yaml``` - применить манифест файл;

```kubectl delete -f deploy-create.yaml``` - удалить сущности из манифест файла;

