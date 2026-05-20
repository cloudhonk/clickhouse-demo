# ClickHouse Helm Chart

This repository contains a Helm chart for deploying [ClickHouse](https://clickhouse.com/) on Kubernetes. ClickHouse is a fast, open-source columnar database management system.

## Prerequisites

- Kubernetes 1.19+
- Helm 3.0+
- Persistent Volume provisioner for storage (if using persistent storage)

## Installation

1. Add Cert Manager

   ```bash
   kubectl apply -f https://github.com/cert-manager/cert-manager/releases/latest/download/cert-manager.yaml
   ```

2. Install the Official ClickHouse Operator Helm Chart

   ```bash
   git clone https://github.com/ClickHouse/clickhouse-operator.git
   helm install clickhouse-operator ./clickhouse-operator/dist/chart
   ```

3. Install ClickHouse Helm Chart

   ```bash
   helm upgrade --install clickhouse ./
   ```
