# Homelab

## Description

This repository serves as a practical lab environment that I set up at home to deepen my understanding of Kubernetes. I firmly believe in learning by doing, so I experiment and acquire new skills through hands-on practice.

All applications are deployed and managed via [Argo CD](https://argo-cd.readthedocs.io/en/stable/) using a GitOps workflow.

## Cluster Architecture

I'm currently using [K3d](https://k3d.io/stable/#releases) to set up my cluster. I found this distribution to be very easy to install and maintain.

## Hardware

I'm running a single-node cluster on the following hardware:

- HP ELITEDESK 800 G2 MINI i5-6400T/16GB/240GB SSD

## End User Applications

<table>
    <tr>
        <th>Logo</th>
        <th>Name</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/homarr-labs/dashboard-icons/svg/vaultwarden.svg"></td>
        <td><a href="https://github.com/dani-garcia/vaultwarden">Vaultwarden</a></td>
        <td>Unofficial Bitwarden compatible server written in Rust, providing a lightweight password management solution.</td>
    </tr>
</table>

## Infrastructure

<table>
    <tr>
        <th>Logo</th>
        <th>Name</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/homarr-labs/dashboard-icons/svg/argo-cd.svg"></td>
        <td><a href="https://argo-cd.readthedocs.io/en/stable/">Argo CD</a></td>
        <td>The GitOps tool for Kubernetes. Manages all applications in this cluster declaratively.</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/grafana.svg"></td>
        <td><a href="https://grafana.com/">Grafana</a></td>
        <td>A leading open-source platform for data visualization and monitoring, enabling the creation of interactive and insightful dashboards.</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/prometheus.svg"></td>
        <td><a href="https://prometheus.io/">Prometheus</a></td>
        <td>An open-source monitoring and alerting toolkit that features a powerful time series database and flexible query language for real-time insights.</td>
    </tr>
    <tr>
        <td><img width="32" src="https://www.svgrepo.com/download/374041/renovate.svg"></td>
        <td><a href="https://github.com/renovatebot/renovate">Renovate</a></td>
        <td>Automated dependency management tool that simplifies keeping your projects up-to-date and secure by handling updates seamlessly.</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/homarr-labs/dashboard-icons/svg/sealed-secrets.svg"></td>
        <td><a href="https://github.com/bitnami-labs/sealed-secrets">Sealed Secrets</a></td>
        <td>Kubernetes controller and tool for one-way encrypted Secrets, enabling safe storage of secrets in Git.</td>
    </tr>
    <tr>
        <td><img width="32" src="https://cdn.jsdelivr.net/gh/walkxcode/dashboard-icons/svg/traefik.svg"></td>
        <td><a href="https://traefik.io/traefik/">Traefik</a></td>
        <td>Modern HTTP reverse proxy and load balancer that makes deploying microservices easy.</td>
    </tr>
</table>

## Secret Management

Secrets are managed using [Sealed Secrets](https://github.com/bitnami-labs/sealed-secrets). Sensitive data is encrypted and stored safely in this Git repository. Only the Sealed Secrets controller running in the cluster can decrypt them.
