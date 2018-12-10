# ocp-test
OpenShift Container Platform brings together Docker and Kubernetes, and provides an API to manage these services. OpenShift Container Platform allows you to create and manage containers.

# Why Should I Use OpenShift?
Containers are standalone processes that run within their own environment, independent of operating system and the underlying infrastructure. OpenShift helps you to develop, deploy, and manage container-based applications. It provides you with a self-service platform to create, modify, and deploy applications on demand, thus enabling faster development and release life cycles.

Think of images as cookie cutters and containers as the actual cookies.

Think of OpenShift as an operating system, images as applications that you run on them, and the containers as the actual running instances of those applications.

# Design Architecture
An APB is a lightweight application definition that borrows several concepts from the Nulecule and Atomicapp projects, namely the concept of a short-lived container with the sole purpose of orchestrating the deployment of the intended application. For the case of APBs, this short-lived container is the APB itself: a container with an Ansible runtime environment plus any files required to assist in orchestration, such as playbooks, roles, and extra dependencies.

The OpenShift Ansible broker (OAB) is an implementation of the Open Service Broker (OSB) API that manages applications defined by APBs. The OAB is supported and deployed by default starting in OpenShift Container Platform 3.7.

Specification of an APB is intended to be lightweight, consisting of several named playbooks and a metadata file to capture information such as parameters to pass into the application.
