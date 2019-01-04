This exercise contains deployment of a simple docker formatter image using DockerFile in openshift.

Steps:

1. git clone http://this-repo
2. oc login -u developer -p developer
3. oc new-project docker-build
4. oc new-app --name echo --insecure-registry http://this-git-repo
5. oc logs -f bc/echo
6. oc get pod
7. oc logs echo-1[application-pod-name] (Exclude the builder image pod as it will be deleted later)
8. oc describe is echo  (Describe the image stream)
9. oc describe bc echo
10. oc describe dc echo
