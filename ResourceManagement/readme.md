### Resource Management

### Labels and Selectors
 - Identify and group resources meaningfully
 - Labels are not unique, multiple objects can have the same label.
 - Think of labels as tags or stickers on Kubernetes objects (Pods, Services, Deployments, etc.)
 - Selectors are used to find or target resources that have a specific set of labels.
 - Selectors are of Different Types: 1) Equality Based selectors  2) Set based Selectors
 - It is the work of selectors to pick pods based on their labels.

### Hands-on Labels and Selectors
  - kubectl get pods -L app -L tier ( To check the labels )
  - kubectl get pod -l 'tier=frontend,app=color-api' ( and condition in Labels )
  - kubectl get pod -l 'tier in (frontend)'

### Selecting Objects with MatchLabels and MatchExpressions
   - if we use matchExpressions then
         matchExpressions:                             matchExpressions:                     matchExpressions:                     
               - key:                                          - key                                - key: managed
                 operator: DOES NOT EXIST                        operator: NOTIn                      operator: Exists
                                                                 values:
                                                                  - canary


### Annotations
  - Add useful information and configuration to resources.
  - Often used by Tools or Kubernetes system itself.

### Namespaces
  - Improve Isolation for groups of resources.
  - Initial Namespaces: default, kube-system, kube-public and kube-node-lease

 ## Hands-on Creating and Managing Namespace 
  - 
