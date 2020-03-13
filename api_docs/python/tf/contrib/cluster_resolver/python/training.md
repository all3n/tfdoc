<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.contrib.cluster_resolver.python.training" />
<meta itemprop="path" content="Stable" />
</div>

# Module: tf.contrib.cluster_resolver.python.training

Library Imports for Cluster Resolvers.

## Modules

[`tpu_cluster_resolver`](../../../../tf/contrib/cluster_resolver/python/training/tpu_cluster_resolver.md) module: Stub file for TPUClusterResolver to maintain backwards compatibility.

## Classes

[`class ClusterResolver`](../../../../tf/contrib/cluster_resolver/ClusterResolver.md): Abstract class for all implementations of ClusterResolvers.

[`class GceClusterResolver`](../../../../tf/contrib/cluster_resolver/GceClusterResolver.md): Cluster Resolver for Google Compute Engine.

[`class KubernetesClusterResolver`](../../../../tf/contrib/cluster_resolver/KubernetesClusterResolver.md): Cluster Resolver for Kubernetes.

[`class SimpleClusterResolver`](../../../../tf/contrib/cluster_resolver/SimpleClusterResolver.md): Simple implementation of ClusterResolver that accepts a ClusterSpec.

[`class SlurmClusterResolver`](../../../../tf/contrib/cluster_resolver/SlurmClusterResolver.md): Cluster Resolver for system with Slurm workload manager.

[`class TFConfigClusterResolver`](../../../../tf/contrib/cluster_resolver/TFConfigClusterResolver.md): Implementation of a ClusterResolver which reads the TF_CONFIG EnvVar.

[`class TPUClusterResolver`](../../../../tf/contrib/cluster_resolver/TPUClusterResolver.md): Cluster Resolver for Google Cloud TPUs.

[`class UnionClusterResolver`](../../../../tf/contrib/cluster_resolver/UnionClusterResolver.md): Performs a union on underlying ClusterResolvers.

