## 1.1 Pod

| Yaml                                                         | Summary                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| pod/pod-dummy.yaml| Start a dummy pod with a dead sleep loop                     |
| pod/pod-nginx.yaml | Start a pod of sample app(nginx)                             |
| pod/pod-initcontainer-sysctl.yaml | Use initContainer to run sysctl, when starting a Pod         |
| pod/pod-healthcheck-nginx.yaml | Start pod with tcp and http healthcheck                      |
| pod/pod-secrets.yaml | Pod use secrets as either volumes or environment variables   |
| pod/pod-gitclone.yaml | Pod: use initContainer as sidecar to web host a git repo     |
| pod/pod-hostaliases.yaml | Pod: add alias to /etc/hosts                                 |
| pod/pod-serviceaccount.yaml | Start pod with serviceaccount, instead of default serviceaccount |
| pod/pod-handlers.yaml | Pod’s events whenever it get started or stoppped             |

## 1.2 Volume

| Yaml                                                         | Summary                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| volume/volume-manual-pv.yaml | Create pv first, then pvc                                    |
| volume/volume-mount-localpath.yaml | Mount a local folder to pods                                 |
| volume/volume-emptydir.yaml | Create a empty folder, then mount to pods                    |
| volume/volume-ebs.yaml | Mount EBS volume to pod running in amazon instance with the same AZ |
| volume/volume-nfs.yaml | Create nfs pv                                                |
| volume/volume-gcePersistentDisk.yaml | Mount GCE disk to pod running in amazon instance with the same AZ |
| volume/volume-digitalocean.yaml | Create DigitalOcean volume for your kubernetes cluster in DigitalOcean |

## 1.3 Service

| Yaml                                                         | Summary                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| service/service-loadbalancer.yaml | Service: loadbalancer                                        |
| service/service-nodeport.yaml | Service: nodeport                                            |
| service/service-ingress.yaml | Service: ingress                                             |
| service/service-clusterip-nginx.yaml | Service: nginx with clusterip                                |
| service/service-cassandra.yaml | Service: cassandra                                           |

## 1.4 Configmap/Envs

| Yaml                                                         | Summary                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------- |
| config/pod-configmap.yaml | Create configmap from file, then use it as a pod volume |
| config/pod-environment-var.yaml | Start a pod passing environment variables               |
| config/pod-env-metada.yaml | Expose metadata to pods                                 |
| config/configmap-plaintext.yaml | Define configmap with plain text                        |

## 1.5 Security - RBAC

| Yaml                                                         | Summary                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| rbac/serviceaccount-default.yaml | Serviceaccount: basic usage                                  |
| rbac/rbac-default.yaml | Serviceaccount: concret example                              |

## 1.6 Security - PodSecurityPolicy

| Yaml                                                         | Summary                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| podsecurity/securitycontext-user.yaml | Configure userid, at both pod and container levels           |
| podsecurity/podsecurity-privileged.yaml | Create pod security with privileged access                   |
| podsecurity/podsecurity-restricted.yaml | Create pod security with restricted access, then apply it later |
| podsecurity/podsecurity-enforce.yaml | Enforce policy security by defining role and cluster role    |
| podsecurity/podsecurity-advanced.yaml | A more complicated definition of pod security policy         |
| podsecurity/podsecurity-example.yaml | A full example with everything included                      |


## 1.7 Security - NetworkPolicy

| Yaml                                                         | Summary                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| networksecurity/networksecurity-denyall-ingress.yaml | Allow all ingress                                            |
| networksecurity/networksecurity-allowall-ingress.yaml | Deny all ingress                                             |
| networksecurity/networksecurity-denyall.yaml | Deny all ingress and egress                                  |
| networksecurity/networksecurity-pod.yaml | Whitelist traffic control                                    |
| networksecurity/networksecurity-complicated.yaml | A comprehensive network policy example                       |
| networksecurity/networksecurity-port.yaml | Allow TCP 443 from one namespace                             |
| networksecurity/networksecurity-deny-othernamespaces.yaml | Deny all ingress traffic from other namespaces               |
| networksecurity/networksecurity-denyegress-exceptdns.yaml | Deny all egress traffic except DNS                           |

## 1.8 Quota & Limits

| Yaml                                                         | Summary                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| quota/limitrange-pvc-size.yaml | LimitRange: PVC size                                         |
| quota/limitrange-pvc-cumulative-size.yaml | ResourceQuota: pvc count and storage size                    |
| quota/limitrange-mem-size.yaml | LimitRange: Pod ram usage. Then apply it to namespace        |

## 1.9 Deployment

| Yaml                                                         | Summary                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| deployment/deployment-nginx.yaml | Deploy nginx with 2 replicas                                 |
| deployment/deployment-mysql.yaml | Deploy mysql                                                 |

## 1.10 Statefulset

| Yaml                                                         | Summary                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| statefulset/statefulset-nginx.yaml | Statefulset: nginx                                           |
| statefulset/statefulset-single-mysql | Statefulset: mysql                                           |
| statefulset/statefulset-replicated-cassandra.yaml | Statefulset: single cassandra                                |
| statefulset/statefulset-replicated-mysql | Statefulset: cassandra with replicas                         |

## 1.11 Jobs & CronJob

| Yaml                                                         | Summary                         |
| ------------------------------------------------------------ | ------------------------------- |
| job/job-affinity.yaml | Deploy a job with node affinity |

## 1.12 HorizontalPodAutoscaler

| Yaml                                                         | Summary                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------- |
| hpa/hpa-nginx.yaml | Deploy a horizontal pod autoscaler for nginx deployment |


## 1.14 Related Tools

| Name                                                         | Summary                                         |
| ------------------------------------------------------------ | ----------------------------------------------- |
| [GitHub: kubernetes-sigs/kustomize](https://github.com/kubernetes-sigs/kustomize) | Customization of kubernetes YAML configurations |