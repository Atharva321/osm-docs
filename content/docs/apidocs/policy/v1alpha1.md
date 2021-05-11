---
title: "Policy v1alpha1 API Reference"
description: "Policy v1alpha1 API reference documentation."
type: docs
---
<p>Packages:</p>
<ul>
<li>
<a href="#policy.openservicemesh.io%2fv1alpha1">policy.openservicemesh.io/v1alpha1</a>
</li>
</ul>
<h2 id="policy.openservicemesh.io/v1alpha1">policy.openservicemesh.io/v1alpha1</h2>
<p>
<p>Package v1alpha1 is the v1alpha1 version of the API.</p>
</p>
Resource Types:
<ul></ul>
<h3 id="policy.openservicemesh.io/v1alpha1.Egress">Egress
</h3>
<p>
<p>Egress is the type used to represent an Egress traffic policy.
An Egress policy allows applications to access endpoints
external to the service mesh or cluster based on the specified
rules in the policy.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>metadata</code><br/>
<em>
<a href="https://v1-18.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.18/#objectmeta-v1-meta">
Kubernetes meta/v1.ObjectMeta
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Object&rsquo;s metadata</p>
Refer to the Kubernetes API documentation for the fields of the
<code>metadata</code> field.
</td>
</tr>
<tr>
<td>
<code>spec</code><br/>
<em>
<a href="#policy.openservicemesh.io/v1alpha1.EgressSpec">
EgressSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Spec is the Egress policy specification</p>
<br/>
<br/>
<table>
<tr>
<td>
<code>sources</code><br/>
<em>
<a href="#policy.openservicemesh.io/v1alpha1.SourceSpec">
[]SourceSpec
</a>
</em>
</td>
<td>
<p>Sources defines the list of sources the Egress policy is applicable to</p>
</td>
</tr>
<tr>
<td>
<code>hosts</code><br/>
<em>
[]string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Hosts defines the list of external hosts the Egress policy should allow</p>
</td>
</tr>
<tr>
<td>
<code>ipAddresses</code><br/>
<em>
[]string
</em>
</td>
<td>
<em>(Optional)</em>
<p>IPAddresses defines the list of external IP addresses the Egress policy is applicable to</p>
</td>
</tr>
<tr>
<td>
<code>ports</code><br/>
<em>
<a href="#policy.openservicemesh.io/v1alpha1.PortSpec">
[]PortSpec
</a>
</em>
</td>
<td>
<p>Ports defines the list of ports the Egress policy is applicable to</p>
</td>
</tr>
<tr>
<td>
<code>matches</code><br/>
<em>
<a href="https://v1-18.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.18/#typedlocalobjectreference-v1-core">
[]Kubernetes core/v1.TypedLocalObjectReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Matches defines the list of routes the Egress policy should match on</p>
</td>
</tr>
</table>
</td>
</tr>
</tbody>
</table>
<h3 id="policy.openservicemesh.io/v1alpha1.EgressSpec">EgressSpec
</h3>
<p>
(<em>Appears on:</em><a href="#policy.openservicemesh.io/v1alpha1.Egress">Egress</a>)
</p>
<p>
<p>EgressSpec is the type used to represent the Egress policy specification</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>sources</code><br/>
<em>
<a href="#policy.openservicemesh.io/v1alpha1.SourceSpec">
[]SourceSpec
</a>
</em>
</td>
<td>
<p>Sources defines the list of sources the Egress policy is applicable to</p>
</td>
</tr>
<tr>
<td>
<code>hosts</code><br/>
<em>
[]string
</em>
</td>
<td>
<em>(Optional)</em>
<p>Hosts defines the list of external hosts the Egress policy should allow</p>
</td>
</tr>
<tr>
<td>
<code>ipAddresses</code><br/>
<em>
[]string
</em>
</td>
<td>
<em>(Optional)</em>
<p>IPAddresses defines the list of external IP addresses the Egress policy is applicable to</p>
</td>
</tr>
<tr>
<td>
<code>ports</code><br/>
<em>
<a href="#policy.openservicemesh.io/v1alpha1.PortSpec">
[]PortSpec
</a>
</em>
</td>
<td>
<p>Ports defines the list of ports the Egress policy is applicable to</p>
</td>
</tr>
<tr>
<td>
<code>matches</code><br/>
<em>
<a href="https://v1-18.docs.kubernetes.io/docs/reference/generated/kubernetes-api/v1.18/#typedlocalobjectreference-v1-core">
[]Kubernetes core/v1.TypedLocalObjectReference
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Matches defines the list of routes the Egress policy should match on</p>
</td>
</tr>
</tbody>
</table>
<h3 id="policy.openservicemesh.io/v1alpha1.PortSpec">PortSpec
</h3>
<p>
(<em>Appears on:</em><a href="#policy.openservicemesh.io/v1alpha1.EgressSpec">EgressSpec</a>)
</p>
<p>
<p>PortSpec is the type used to represent the Port in the list of Ports specified in an Egress policy specification</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>number</code><br/>
<em>
int
</em>
</td>
<td>
<p>Number defines the port number</p>
</td>
</tr>
<tr>
<td>
<code>protocol</code><br/>
<em>
string
</em>
</td>
<td>
<p>Protocol defines the protocol served by the port</p>
</td>
</tr>
</tbody>
</table>
<h3 id="policy.openservicemesh.io/v1alpha1.SourceSpec">SourceSpec
</h3>
<p>
(<em>Appears on:</em><a href="#policy.openservicemesh.io/v1alpha1.EgressSpec">EgressSpec</a>)
</p>
<p>
<p>SourceSpec is the type used to represent the Source in the list of Sources specified in an Egress policy specification</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>kind</code><br/>
<em>
string
</em>
</td>
<td>
<p>Kind defines the kind for the source in the Egress policy, ex. ServiceAccount</p>
</td>
</tr>
<tr>
<td>
<code>name</code><br/>
<em>
string
</em>
</td>
<td>
<p>Name defines the name of the source for the given Kind</p>
</td>
</tr>
<tr>
<td>
<code>namespace</code><br/>
<em>
string
</em>
</td>
<td>
<p>Namespace defines the namespace for the given source</p>
</td>
</tr>
</tbody>
</table>
<hr/>
<p><em>
Generated with <code>gen-crd-api-reference-docs</code>
on git commit <code>43a55c3b</code>.
</em></p>