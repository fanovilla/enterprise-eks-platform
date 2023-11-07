An enterprise multi-tenant EKS (Amazon Elastic Kubernetes Service) platform serves multiple teams or departments within an organization. Managing such a platform involves several key requirements to ensure security, isolation, scalability, and ease of management. Here are some usual requirements for an enterprise multi-tenant EKS platform:

1. **Multi-Tenancy Isolation**:
    - **Namespaces**: Implement a robust namespace-based isolation strategy to separate resources and workloads of different tenants. Each team or department should have its own namespace.
    - **Network Isolation**: Ensure that tenants' pods and services are isolated from each other at the network level using Kubernetes Network Policies and security groups.

2. **RBAC and IAM Integration**:
    - Implement Role-Based Access Control (RBAC) within Kubernetes to define who can perform what actions within each namespace.
    - Integrate with AWS Identity and Access Management (IAM) for authentication and authorization, allowing IAM roles to be assigned to Kubernetes service accounts.

3. **Resource Quotas and Limits**:
    - Set up resource quotas and limits for each tenant to prevent resource hogging and ensure fair resource allocation.

4. **Monitoring and Logging**:
    - Implement comprehensive monitoring and logging for each tenant using tools like Prometheus, Grafana, and Fluentd.
    - Provide tenants with access to their own monitoring dashboards.

5. **Managed Services Integration**:
    - Integrate with AWS managed services, such as RDS for databases, to simplify data storage and management for tenants.

6. **Ingress and Load Balancing**:
    - Provide isolation for Ingress controllers and load balancers, allowing tenants to have their own routing and TLS configurations.

7. **CI/CD Integration**:
    - Facilitate CI/CD pipelines for tenants, allowing them to deploy, update, and manage their applications efficiently.

8. **Backup and Disaster Recovery**:
    - Implement backup and disaster recovery solutions to ensure data protection and high availability for tenant workloads.

9. **Security Policies and Compliance**:
    - Define and enforce security policies, ensuring compliance with industry standards and organizational requirements.
    - Regularly audit and scan tenant workloads for vulnerabilities and compliance violations.

10. **Automation and Self-Service**:
    - Create self-service portals or tools that enable tenants to provision, scale, and manage their resources within the EKS cluster.

11. **Cost Allocation and Control**:
    - Implement mechanisms for tracking and allocating costs to different tenants.
    - Enforce cost control measures and set budgets for each tenant.

12. **Scaling and Resource Management**:
    - Implement auto-scaling policies and resource management to ensure optimal resource utilization and cost efficiency.

13. **High Availability**:
    - Design the EKS cluster for high availability with multi-AZ deployment to ensure minimal downtime.

14. **Documentation and Training**:
    - Maintain comprehensive documentation for tenants, including best practices, guidelines, and procedures.
    - Provide training and support to tenant teams to help them manage their workloads effectively.

15. **Governance and Compliance**:
    - Establish clear governance policies and procedures for managing the multi-tenant EKS environment.
    - Ensure compliance with data protection regulations, such as GDPR, if applicable.

16. **Integration with Identity Providers**:
    - Integrate with your organization's identity providers (e.g., LDAP, Active Directory) to manage tenant authentication and authorization.

17. **Elasticity and Scalability**:
    - Design the platform to easily scale by adding more nodes, node groups, or clusters as needed.

18. **Versioning and Upgrades**:
    - Plan for Kubernetes and EKS version upgrades and ensure that tenant workloads remain compatible.

19. **Secrets Management**:
    - Implement robust secrets management solutions to securely store and manage sensitive information needed by tenant applications.

20. **Disaster Recovery Planning**:
    - Develop and test disaster recovery plans to minimize downtime in case of critical failures.

Building and managing a multi-tenant EKS platform is a complex task that requires careful planning and adherence to best practices. It's essential to strike a balance between isolation and resource efficiency while ensuring the platform meets the needs of different tenants within the organization.