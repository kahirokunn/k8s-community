# Contributing to SIG Multicluster

Welcome to the Kubernetes SIG Multicluster contributing guide. We are excited
about the prospect of you joining our [community][SIG community page]!

SIG Multicluster maintains APIs, libraries, tests, and documentation in several
subproject repositories. Choose the repository that owns the resource or
workflow you want to change before opening an issue or pull request. The
[charter](charter.md) defines the SIG's scope and governance. The SIG website
also maintains a [contributing overview][website contributing guide].

## Find the right repository

| If you want to work on | Start here | Representative resources |
| --- | --- | --- |
| Properties published by an individual cluster | [about-api issues] | `ClusterProperty` |
| Cluster metadata, access information, or placement output | [cluster-inventory-api issues] | `ClusterProfile`, `PlacementDecision` |
| Services shared across clusters | [mcs-api issues] | `ServiceExport`, `ServiceImport` |
| Resources delivered from a hub cluster to spoke clusters | [work-api issues] | `Work`, `AppliedWork` |
| A reusable library for multicluster controllers | [multicluster-runtime issues] | providers, managers, multicluster reconcilers |
| SIG concepts, implementation guidance, or the public website | [sig-multicluster-site issues] | [multicluster.sigs.k8s.io](https://multicluster.sigs.k8s.io/) content |

See the generated [subprojects list][SIG subprojects] for the current list of
subprojects and their owners.

For a question that spans subprojects, ask in
[#sig-multicluster on Kubernetes Slack][slack] (an invitation is available at
[slack.k8s.io][slack-signup]). Major design discussions and
announcements also use the [mailing list] and the regular [SIG meeting]. To
notify the right reviewers on GitHub, mention one of the teams listed in the
[SIG contact information][SIG contact].

## Before you begin

- Follow the Kubernetes [Code of Conduct].
- Sign the Kubernetes [Contributor License Agreement].
- Read the general [contributor guide] and the selected repository's README and
  contributing instructions.
- Search that repository for an existing issue or proposal before starting
  work.

New contributors can look for issues labeled [`help wanted` or `good first
issue`][help wanted]. If no suitable issue is available, ask in Slack or at a SIG meeting;
maintainers can identify work for which review time is available.

## Report a bug

Open the issue in the repository that owns the affected API or library. Include:

- the API, client, controller, and Kubernetes versions involved,
- the manifests or commands needed to reproduce the problem,
- the expected and actual behavior,
- logs or status conditions that help explain the failure.

If the problem belongs to a product that implements a SIG API, report it to
that implementation's repository rather than the API specification repository.

## Propose an API or behavior change

1. Open an issue in the owning subproject and describe the user problem, the
   proposed behavior, and a concrete example.
2. For changes that affect more than one subproject, add the proposal to the
   [SIG meeting agenda] and share it on the mailing list.
3. Use the [Kubernetes Enhancement Proposal process] when the change introduces
   or substantially changes a multicluster API or requires project-wide review.
   SIG Multicluster uses KEPs even when the implementation is out-of-tree and
   not tied to a specific Kubernetes release. Existing proposals are listed
   with the [SIG Multicluster KEPs].
4. Agree on the design and review plan with maintainers before sending a large
   implementation pull request.

Not every bug fix or compatible API clarification requires a KEP. The
subproject maintainers can confirm the appropriate review path in the issue.

Review capacity in SIG Multicluster is limited, and it is normal for members
to push back on a proposal: deferring it to a later release, asking for help
with existing issues first, or suggesting that the problem be solved another
way.

## Send a pull request

Follow the selected repository's development and test instructions. A pull
request should:

- link the issue or proposal it implements,
- include unit, integration, or end-to-end tests appropriate to the change,
- update conformance tests when observable API behavior changes,
- update user-facing documentation and examples,
- use `Fixes #<issue number>` or `Closes #<issue number>` when it fully resolves
  an issue.

Most SIG Multicluster subprojects release independently of the Kubernetes core
release. Changes to Kubernetes core are tracked in [kubernetes/kubernetes]
under the `sig/multicluster` label and must also follow the
[Kubernetes release] and enhancement timelines.

## Escalation

Start by following up with the reviewers and owners in the affected
repository. If an issue or pull request has had no response for a week, raise it
in `#sig-multicluster` or add it to the SIG meeting agenda. Include the link,
the user impact, and the decision or review that is needed.

[Code of Conduct]: /code-of-conduct.md
[Contributor License Agreement]: /CLA.md
[Kubernetes Enhancement Proposal process]: https://git.k8s.io/enhancements/keps/README.md
[Kubernetes release]: https://kubernetes.io/releases/
[SIG Multicluster KEPs]: https://git.k8s.io/enhancements/keps/sig-multicluster
[SIG community page]: /sig-multicluster
[SIG contact]: /sig-multicluster#contact
[SIG meeting]: /sig-multicluster#meetings
[SIG meeting agenda]: https://tinyurl.com/sig-multicluster-notes
[SIG subprojects]: /sig-multicluster#subprojects
[about-api issues]: https://github.com/kubernetes-sigs/about-api/issues
[cluster-inventory-api issues]: https://github.com/kubernetes-sigs/cluster-inventory-api/issues
[contributor guide]: /contributors/guide
[help wanted]: /contributors/guide/help-wanted.md
[kubernetes/kubernetes]: https://github.com/kubernetes/kubernetes
[mailing list]: https://groups.google.com/forum/#!forum/kubernetes-sig-multicluster
[mcs-api issues]: https://github.com/kubernetes-sigs/mcs-api/issues
[multicluster-runtime issues]: https://github.com/kubernetes-sigs/multicluster-runtime/issues
[sig-multicluster-site issues]: https://github.com/kubernetes-sigs/sig-multicluster-site/issues
[slack]: https://kubernetes.slack.com/messages/sig-multicluster
[slack-signup]: https://slack.k8s.io/
[website contributing guide]: https://multicluster.sigs.k8s.io/contributing/
[work-api issues]: https://github.com/kubernetes-sigs/work-api/issues
