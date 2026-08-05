# SIG Multicluster Charter

This charter adheres to the conventions described in the [Kubernetes Charter README] and uses
the Roles and Organization Management outlined in [sig-governance].

## Scope

SIG Multicluster supports platform builders and tool authors whose software
needs to work with more than one Kubernetes cluster. The SIG defines portable,
vendor-neutral APIs and common building blocks so that multicluster tools can
exchange information.

### In scope

#### Code, Binaries and Services

- Portable APIs and conventions for identifying, describing, discovering,
  selecting, and accessing Kubernetes clusters.
- Portable APIs for making Services available across clusters.
- Portable APIs for distributing Kubernetes resources across clusters.
- Reusable libraries for building controllers that reconcile a changing set
  of clusters.
- Client libraries, conformance tests, and documentation for SIG-owned APIs.

Code, binaries, and services are owned through the SIG's
[subprojects][sig-subprojects].

#### Cross-cutting and Externally Facing Processes

- Review and sponsor Kubernetes Enhancement Proposals for SIG-owned APIs.
- Define compatibility and conformance expectations for portable multicluster
  APIs.
- Gather user feedback and document common multicluster use cases and
  terminology.
- Work with [SIG Network] on multicluster Service and networking semantics,
  with [SIG Auth] on credential and access semantics for the cluster inventory
  APIs, and with other SIGs when a multicluster API intersects their areas of
  ownership.
- Review upstream Kubernetes changes that could break established multicluster
  behavior or interoperability.

### Out of scope

- Creating, upgrading, or deleting Kubernetes clusters; those concerns belong
  to [SIG Cluster Lifecycle].
- End-user multicluster management products and vendor-specific
  implementations of SIG APIs.
- Network connectivity and data planes between clusters. Multicluster
  networking is a shared responsibility with [SIG Network]; SIG Multicluster
  defines portable API semantics but does not own the underlying network
  implementation.
- Scheduling algorithms and workload rollout strategies. SIG Multicluster may
  define the interface used to publish a placement or distribute resources,
  but does not own the scheduler that makes the placement decision.

## Roles and Organization Management

This SIG adheres to the Roles and Organization Management outlined in [sig-governance]
and opts-in to updates and modifications to [sig-governance].

### Additional responsibilities of Chairs

- Approve and facilitate the creation and decommissioning of subprojects.
- Review and approve SIG Enhancement Proposals, or delegate this review to
  subproject owners.
- Resolve cross-subproject and cross-SIG technical issues and decisions, or
  delegate to another Lead as needed.

### Deviations from [sig-governance]

- SIG Multicluster does not designate separate Tech Leads because technical
  direction is set per subproject by its owners. Chairs assume the Tech Lead
  responsibilities defined in [sig-governance].

### Subproject Creation

Subprojects may be created with a simple majority vote of SIG Chairs, who
follow the [Subproject Creation process][subproject-creation] defined in
[sig-governance].

[Kubernetes Charter README]: /committee-steering/governance/README.md
[SIG Auth]: /sig-auth
[SIG Cluster Lifecycle]: /sig-cluster-lifecycle
[SIG Network]: /sig-network
[sig-governance]: /committee-steering/governance/sig-governance.md
[sig-subprojects]: /sig-multicluster/README.md#subprojects
[subproject-creation]: /committee-steering/governance/sig-governance.md#subproject-creation
