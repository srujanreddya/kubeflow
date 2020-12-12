# kubeflow profile creation with kustomize
> Instructions to create profiles and add user profiles as contributor.

Clone the `profile-kustomize` branch.

# Creation of Service account profile

```
$ cd base/sa-profile
$ vi params.env # Update values as per your requierment
$ kubectl apply -k . # It will create profile & profile namespace and configmap for user.
```

# Creation of service account PVC

```
$ cd base/sa-pvc
$ vi params.env # Update values as per your requierment
$ kubectl apply -k . # It will create profile & profile namespace and configmap for user.
```

# Creation of User profile

```
$ cd base/user-profile
$ vi params.env # Update values as per your requierment
$ kubectl apply -k . # It will create profile & profile namespace and configmap for user.
```

# Adding user profile as contributor

```
$ cd base/user-contributor
$ vi params.env # Update values as per your requierment
$ kubectl apply -k . # It will create rolebinding & servicerolebinding and configmap for user.
```
