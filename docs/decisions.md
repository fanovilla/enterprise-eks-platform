# cluster topology

https://kubernetes.io/docs/setup/best-practices/cluster-large/
More specifically, Kubernetes is designed to accommodate configurations that meet all of the following criteria:

    No more than 110 pods per node
    No more than 5,000 nodes
    No more than 150,000 total pods
    No more than 300,000 total containers

# service mesh - istio

https://thenewstack.io/which-service-mesh-should-i-use/

supported by AWS EKS Blueprints - https://github.com/aws-ia/terraform-aws-eks-blueprints/tree/main/patterns/istio



# istio topology

https://istio.io/latest/docs/setup/install/multicluster/multi-primary/



# CNI

https://docs.aws.amazon.com/eks/latest/userguide/alternate-cni-plugins.html

The Amazon VPC CNI plugin for Kubernetes is the only CNI plugin supported by Amazon EKS.

Alternate compatible CNI plugins require additional commercial support from Partner.


https://aws.github.io/aws-eks-best-practices/networking/vpc-cni/


# Cluster Autoscaling

Karpenter - https://aws.github.io/aws-eks-best-practices/karpenter/




# Nodes

EKS cluster can schedule Pods on any combination of self-managed nodes, Amazon EKS managed node groups, and AWS Fargate.

Karpenter to manage nodes. Karpenter itself in Fargate - https://aws.github.io/aws-eks-best-practices/karpenter/


https://aws-ia.github.io/terraform-aws-eks-blueprints/patterns/karpenter/



# private cluster

https://aws-ia.github.io/terraform-aws-eks-blueprints/patterns/fully-private-cluster/

https://docs.aws.amazon.com/eks/latest/userguide/private-clusters.html#private-cluster-requirements


# argocd topology

https://akuity.io/blog/argo-cd-architectures-explained/

https://akuity.io/blog/argo-cd-architectures-explained/#The-management-cluster---One-Instance


# mgmt cluster 

https://aws-ia.github.io/terraform-aws-eks-blueprints/patterns/argocd/


# conventional commits

https://www.conventionalcommits.org/en/v1.0.0/


