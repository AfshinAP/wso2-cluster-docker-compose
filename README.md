
# WSO2 Cluster docker-compose

This repository provides a docker-coompose based approach to setting up a WSO2 cluster. It include WSO2 Identity Server, WSO2 API Manager, WSO2 API Gateway, WSO2 Micro Integrator and PostgreSQL database.

## WSO2 Structure

![WSO2](https://github.com/AfshinAP/wso2-cluster-docker-compose/blob/main/WSO2-Cluster-Structure.jpeg?raw=true)

## Architecture

A high-level flow for this cluster:

- WSO2 Identity Server handles user authentication and authorization.
- WSO2 API Manager acts as the control plane for APIs: Publisher, Developer Portal, Key Manager, etc.
- WSO2 API Gateway: Gateway nodes.
- WSO2 Micro Integrator hosts integration services or mediations.
- PostgreSQL store configuration, user credentials, tokens, etc.

## Configuration

- in `deployment.toml`, set yout properties like ip address
- for migrate your database: [changing-to-postgresql](https://apim.docs.wso2.com/en/latest/install-and-setup/setup/setting-up-databases/changing-default-databases/changing-to-postgresql/)
- for config key manager in wso2am: [configure-wso2is7-connector](https://apim.docs.wso2.com/en/latest/administer/key-managers/configure-wso2is7-connector/)
- for config wso2is: [configuring-wso2-is-7-0-as-a-key-manage](https://medium.com/@ash15.sulaiman/configuring-wso2-is-7-0-as-a-key-manager-in-wso2-apim-4-3-0-5493ea9f8eaf)
- for OIDC SSO configuration in wso2am carbon: [oidc-sso-with-wso2](https://sumudusahanweerasuriya.medium.com/wso2-api-manager-portal-oidc-sso-with-wso2-identity-server-7-0-0-c2c786c588f1)

## Deployment

To deploy these docker-composes run

```bash
  docker compose up -d
```