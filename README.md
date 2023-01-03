# Monitoring-Logging

## Description
This project is to create a monitoring system in a way to easy to install and operator.
We have many ways to install and operator, but to be esier to reproduce it in case of disaster is a good choose using one operator.

## Operator
Operator is a CRD that can controlls others deployments or Statefull installations, in that case this can be used to controll the installation of prometheus, alertmanager and Grafana. Beyond to install the prometheus rules and alerts.

## Installation
To install it you just need run these steps below:

 * Add helm repo:
   ```bash
   helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
   ```
 * Update the repo:
   ```bash
   helm repo update
   ```
 * Install chart:
   ```
   helm install prometheus prometheus-community/kube-prometheus-stack
   ```
We are using custom values, so if you need add more feautures please check the entire values in this link:
https://github.com/prometheus-community/helm-charts/blob/main/charts/kube-prometheus-stack/values.yaml

* To apply with the values, do this:

  ```
  helm upgrade --install prometheus prometheus-community/kube-prometheus-stack --namespace monitoring --create-namespace --values values.yaml
  ```

## Usage
To use it you need to install the helm chart and use the CRDs to change something inside the cluster.

## Support
In case of any support contact any person in Helium team

## Roadmap
If you have ideas for releases in the future, it is a good idea to list them in the README.

## Project status
In progress

- [x] Choose the right operator
- [x] Install the operator
- [x] Install the prometheus
- [x] Install Grafana
- [x] Install Alert Manager
- [ ] Choose what you need to monitor
- [ ] Configure the prometheus in other environment clusters
- [ ] Configure the endpoints to the other environments


## Authors and acknowledgment
Franklin Ribeiro - fribeiro@cocus.com
Shay Zadegan - Shaghayegh.Abdollahzadegan@Vodafone.com