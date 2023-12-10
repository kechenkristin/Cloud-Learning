# CKAD Exam Prep

## Res
- gitee note  
  https://gitee.com/yooome/golang/blob/main/21-k8s%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B/Kubernetes%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B.md
- heima k8s tutorial  
  https://www.bilibili.com/video/BV1Qv41167ck/?p=84&spm_id_from=pageDriver&vd_source=a0023377abf1124bf8f6558444cd4535
- udemy tutorial  
  https://www.bilibili.com/video/BV14S4y1c7Sh?p=23&spm_id_from=pageDriver&vd_source=a0023377abf1124bf8f6558444cd4535  
  https://www.udemy.com/course/certified-kubernetes-application-developer/  
- cloud academy lab

## Knowledge
### Core Concepts
#### k8s architecture
#### create and configure pods

### Configuration
#### Config Map
- pre note: environment variables  
  https://gitee.com/yooome/golang/blob/main/21-k8s%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B/Kubernetes%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B.md#524-%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F  
- note & lab  
  https://gitee.com/yooome/golang/blob/main/21-k8s%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B/Kubernetes%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B.md#831-configmap

#### Secrets(Similar to Config Map)


#### Security Context
- note  
https://kubernetes.io/docs/tasks/configure-pod-container/security-context/
- lab  
https://cloudacademy.com/lab/mastering-kubernetes-pod-configuration-security-contexts/?context_id=3086&context_resource=lp&training_plan=150922
- video  
  https://www.bilibili.com/video/BV14S4y1c7Sh?p=18&vd_source=a0023377abf1124bf8f6558444cd4535

#### Service Account
- note  
https://kubernetes.io/docs/concepts/security/service-accounts/

- lab  
  https://cloudacademy.com/lab/mastering-kubernetes-pod-configuration-service-accounts/?context_id=3086&context_resource=lp&training_plan=150922  

- video    
  https://www.bilibili.com/video/BV14S4y1c7Sh?p=20&vd_source=a0023377abf1124bf8f6558444cd4535

#### Resource Requirement
- note  
  https://gitee.com/yooome/golang/blob/main/21-k8s%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B/Kubernetes%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B.md#526-%E8%B5%84%E6%BA%90%E9%85%8D%E9%A2%9D

- lab  
  https://cloudacademy.com/lab/mastering-kubernetes-pod-configuration-defining-resource-requirements/requesting-and-limiting-resources-pods/?context_id=3086&context_resource=lp&training_plan=150922
  - auto completion  
  `source <(kubectl completion bash)`
  - top: top 命令类似于本机 Linux top 命令，用于测量进程的 CPU 和内存使用情况。您可以在节点或 Pod 级别进行监控。  
  `kubectl top --help`
  - resources configure  
  `kubectl explain pod.spec.containers.resources`
  - Rules
    - Containers that exceed their memory limits will be terminated and restarted if possible.
    - Containers that exceed their memory request may be evicted when the node runs out of memory.
    - Containers that exceed their CPU limits may be allowed to exceed the limit depending on the other Pods on the node. Containers will not be terminated for exceeding CPU limits.
