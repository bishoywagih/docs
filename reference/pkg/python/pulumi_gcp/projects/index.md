<div class="section" id="module-pulumi_gcp.projects">
<span id="projects"></span><h1>projects<a class="headerlink" href="#module-pulumi_gcp.projects" title="Permalink to this headline">¶</a></h1>
<dl class="class">
<dt id="pulumi_gcp.projects.IAMBinding">
<em class="property">class </em><code class="descclassname">pulumi_gcp.projects.</code><code class="descname">IAMBinding</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>members=None</em>, <em>project=None</em>, <em>role=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMBinding" title="Permalink to this definition">¶</a></dt>
<dd><p>Three different resources help you manage your IAM policy for a project. Each of these resources serves a different use case:</p>
<ul class="simple">
<li><cite>google_project_iam_policy</cite>: Authoritative. Sets the IAM policy for the project and replaces any existing policy already attached.</li>
<li><cite>google_project_iam_binding</cite>: Authoritative for a given role. Updates the IAM policy to grant a role to a list of members. Other roles within the IAM policy for the project are preserved.</li>
<li><cite>google_project_iam_member</cite>: Non-authoritative. Updates the IAM policy to grant a role to a new member. Other members for the role for the project are preserved.</li>
</ul>
<p>&gt; <strong>Note:</strong> <cite>google_project_iam_policy</cite> <strong>cannot</strong> be used in conjunction with <cite>google_project_iam_binding</cite> and <cite>google_project_iam_member</cite> or they will fight over what your policy should be.</p>
<p>&gt; <strong>Note:</strong> <cite>google_project_iam_binding</cite> resources <strong>can be</strong> used in conjunction with <cite>google_project_iam_member</cite> resources <strong>only if</strong> they do not grant privilege to the same role.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<p>:param pulumi.Input[list] members
:param pulumi.Input[str] project: The project ID. If not specified, uses the</p>
<blockquote>
<div>ID of the project configured with the provider.</div></blockquote>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><strong>role</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The role that should be applied. Only one
<cite>google_project_iam_binding</cite> can be used per role. Note that custom roles must be of the format
<cite>[projects|organizations]/{parent-name}/roles/{role-name}</cite>.</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMBinding.etag">
<code class="descname">etag</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMBinding.etag" title="Permalink to this definition">¶</a></dt>
<dd><p>(Computed) The etag of the project’s IAM policy.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMBinding.project">
<code class="descname">project</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMBinding.project" title="Permalink to this definition">¶</a></dt>
<dd><p>The project ID. If not specified, uses the
ID of the project configured with the provider.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMBinding.role">
<code class="descname">role</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMBinding.role" title="Permalink to this definition">¶</a></dt>
<dd><p>The role that should be applied. Only one
<cite>google_project_iam_binding</cite> can be used per role. Note that custom roles must be of the format
<cite>[projects|organizations]/{parent-name}/roles/{role-name}</cite>.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.IAMBinding.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMBinding.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.IAMBinding.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMBinding.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_gcp.projects.IAMCustomRole">
<em class="property">class </em><code class="descclassname">pulumi_gcp.projects.</code><code class="descname">IAMCustomRole</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>deleted=None</em>, <em>description=None</em>, <em>permissions=None</em>, <em>project=None</em>, <em>role_id=None</em>, <em>stage=None</em>, <em>title=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMCustomRole" title="Permalink to this definition">¶</a></dt>
<dd><p>Allows management of a customized Cloud IAM project role. For more information see
[the official documentation](<a class="reference external" href="https://cloud.google.com/iam/docs/understanding-custom-roles">https://cloud.google.com/iam/docs/understanding-custom-roles</a>)
and
[API](<a class="reference external" href="https://cloud.google.com/iam/reference/rest/v1/projects.roles">https://cloud.google.com/iam/reference/rest/v1/projects.roles</a>).</p>
<dl class="docutils">
<dt>&gt; <strong>Warning:</strong> Note that custom roles in GCP have the concept of a soft-delete. There are two issues that may arise</dt>
<dd>from this and how roles are propagated. 1) creating a role may involve undeleting and then updating a role with the
same name, possibly causing confusing behavior between undelete and update. 2) A deleted role is permanently deleted
after 7 days, but it can take up to 30 more days (i.e. between 7 and 37 days after deletion) before the role name is
made available again. This means a deleted role that has been deleted for more than 7 days cannot be changed at all
by Terraform, and new roles cannot share that name.</dd>
</dl>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<p>:param pulumi.Input[bool] deleted
:param pulumi.Input[str] description: A human-readable description for the role.
:param pulumi.Input[list] permissions: The names of the permissions this role grants when bound in an IAM policy. At least one permission must be specified.
:param pulumi.Input[str] project: The project that the service account will be created in.</p>
<blockquote>
<div>Defaults to the provider project configuration.</div></blockquote>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>role_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The role id to use for this role.</li>
<li><strong>stage</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The current launch stage of the role.
Defaults to <cite>GA</cite>.
List of possible stages is [here](<a class="reference external" href="https://cloud.google.com/iam/reference/rest/v1/organizations.roles#Role.RoleLaunchStage">https://cloud.google.com/iam/reference/rest/v1/organizations.roles#Role.RoleLaunchStage</a>).</li>
<li><strong>title</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – A human-readable title for the role.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMCustomRole.description">
<code class="descname">description</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMCustomRole.description" title="Permalink to this definition">¶</a></dt>
<dd><p>A human-readable description for the role.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMCustomRole.permissions">
<code class="descname">permissions</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMCustomRole.permissions" title="Permalink to this definition">¶</a></dt>
<dd><p>The names of the permissions this role grants when bound in an IAM policy. At least one permission must be specified.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMCustomRole.project">
<code class="descname">project</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMCustomRole.project" title="Permalink to this definition">¶</a></dt>
<dd><p>The project that the service account will be created in.
Defaults to the provider project configuration.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMCustomRole.role_id">
<code class="descname">role_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMCustomRole.role_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The role id to use for this role.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMCustomRole.stage">
<code class="descname">stage</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMCustomRole.stage" title="Permalink to this definition">¶</a></dt>
<dd><p>The current launch stage of the role.
Defaults to <cite>GA</cite>.
List of possible stages is [here](<a class="reference external" href="https://cloud.google.com/iam/reference/rest/v1/organizations.roles#Role.RoleLaunchStage">https://cloud.google.com/iam/reference/rest/v1/organizations.roles#Role.RoleLaunchStage</a>).</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMCustomRole.title">
<code class="descname">title</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMCustomRole.title" title="Permalink to this definition">¶</a></dt>
<dd><p>A human-readable title for the role.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.IAMCustomRole.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMCustomRole.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.IAMCustomRole.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMCustomRole.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_gcp.projects.IAMMember">
<em class="property">class </em><code class="descclassname">pulumi_gcp.projects.</code><code class="descname">IAMMember</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>member=None</em>, <em>project=None</em>, <em>role=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMMember" title="Permalink to this definition">¶</a></dt>
<dd><p>Three different resources help you manage your IAM policy for a project. Each of these resources serves a different use case:</p>
<ul class="simple">
<li><cite>google_project_iam_policy</cite>: Authoritative. Sets the IAM policy for the project and replaces any existing policy already attached.</li>
<li><cite>google_project_iam_binding</cite>: Authoritative for a given role. Updates the IAM policy to grant a role to a list of members. Other roles within the IAM policy for the project are preserved.</li>
<li><cite>google_project_iam_member</cite>: Non-authoritative. Updates the IAM policy to grant a role to a new member. Other members for the role for the project are preserved.</li>
</ul>
<p>&gt; <strong>Note:</strong> <cite>google_project_iam_policy</cite> <strong>cannot</strong> be used in conjunction with <cite>google_project_iam_binding</cite> and <cite>google_project_iam_member</cite> or they will fight over what your policy should be.</p>
<p>&gt; <strong>Note:</strong> <cite>google_project_iam_binding</cite> resources <strong>can be</strong> used in conjunction with <cite>google_project_iam_member</cite> resources <strong>only if</strong> they do not grant privilege to the same role.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<p>:param pulumi.Input[str] member
:param pulumi.Input[str] project: The project ID. If not specified, uses the</p>
<blockquote>
<div>ID of the project configured with the provider.</div></blockquote>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><strong>role</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The role that should be applied. Only one
<cite>google_project_iam_binding</cite> can be used per role. Note that custom roles must be of the format
<cite>[projects|organizations]/{parent-name}/roles/{role-name}</cite>.</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMMember.etag">
<code class="descname">etag</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMMember.etag" title="Permalink to this definition">¶</a></dt>
<dd><p>(Computed) The etag of the project’s IAM policy.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMMember.project">
<code class="descname">project</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMMember.project" title="Permalink to this definition">¶</a></dt>
<dd><p>The project ID. If not specified, uses the
ID of the project configured with the provider.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMMember.role">
<code class="descname">role</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMMember.role" title="Permalink to this definition">¶</a></dt>
<dd><p>The role that should be applied. Only one
<cite>google_project_iam_binding</cite> can be used per role. Note that custom roles must be of the format
<cite>[projects|organizations]/{parent-name}/roles/{role-name}</cite>.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.IAMMember.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMMember.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.IAMMember.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMMember.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_gcp.projects.IAMPolicy">
<em class="property">class </em><code class="descclassname">pulumi_gcp.projects.</code><code class="descname">IAMPolicy</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>authoritative=None</em>, <em>disable_project=None</em>, <em>policy_data=None</em>, <em>project=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMPolicy" title="Permalink to this definition">¶</a></dt>
<dd><p>Three different resources help you manage your IAM policy for a project. Each of these resources serves a different use case:</p>
<ul class="simple">
<li><cite>google_project_iam_policy</cite>: Authoritative. Sets the IAM policy for the project and replaces any existing policy already attached.</li>
<li><cite>google_project_iam_binding</cite>: Authoritative for a given role. Updates the IAM policy to grant a role to a list of members. Other roles within the IAM policy for the project are preserved.</li>
<li><cite>google_project_iam_member</cite>: Non-authoritative. Updates the IAM policy to grant a role to a new member. Other members for the role for the project are preserved.</li>
</ul>
<p>&gt; <strong>Note:</strong> <cite>google_project_iam_policy</cite> <strong>cannot</strong> be used in conjunction with <cite>google_project_iam_binding</cite> and <cite>google_project_iam_member</cite> or they will fight over what your policy should be.</p>
<p>&gt; <strong>Note:</strong> <cite>google_project_iam_binding</cite> resources <strong>can be</strong> used in conjunction with <cite>google_project_iam_member</cite> resources <strong>only if</strong> they do not grant privilege to the same role.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
<li><strong>authoritative</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – (Optional, only for <cite>google_project_iam_policy</cite>)
A boolean value indicating if this policy
should overwrite any existing IAM policy on the project. When set to true,
<strong>any policies not in your config file will be removed</strong>. This can <strong>lock
you out</strong> of your project until an Organization Administrator grants you
access again, so please exercise caution. If this argument is <cite>true</cite> and you
want to delete the resource, you must set the <cite>disable_project</cite> argument to
<cite>true</cite>, acknowledging that the project will be inaccessible to anyone but the
Organization Admins, as it will no longer have an IAM policy. Rather than using
this, you should use <cite>google_project_iam_binding</cite> and
<cite>google_project_iam_member</cite>.</li>
<li><strong>disable_project</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – (Optional, only for <cite>google_project_iam_policy</cite>)
A boolean value that must be set to <cite>true</cite>
if you want to delete a <cite>google_project_iam_policy</cite> that is authoritative.</li>
<li><strong>policy_data</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The <cite>google_iam_policy</cite> data source that represents
the IAM policy that will be applied to the project. The policy will be
merged with any existing policy applied to the project.</li>
<li><strong>project</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The project ID. If not specified, uses the
ID of the project configured with the provider.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMPolicy.authoritative">
<code class="descname">authoritative</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMPolicy.authoritative" title="Permalink to this definition">¶</a></dt>
<dd><p>(Optional, only for <cite>google_project_iam_policy</cite>)
A boolean value indicating if this policy
should overwrite any existing IAM policy on the project. When set to true,
<strong>any policies not in your config file will be removed</strong>. This can <strong>lock
you out</strong> of your project until an Organization Administrator grants you
access again, so please exercise caution. If this argument is <cite>true</cite> and you
want to delete the resource, you must set the <cite>disable_project</cite> argument to
<cite>true</cite>, acknowledging that the project will be inaccessible to anyone but the
Organization Admins, as it will no longer have an IAM policy. Rather than using
this, you should use <cite>google_project_iam_binding</cite> and
<cite>google_project_iam_member</cite>.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMPolicy.disable_project">
<code class="descname">disable_project</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMPolicy.disable_project" title="Permalink to this definition">¶</a></dt>
<dd><p>(Optional, only for <cite>google_project_iam_policy</cite>)
A boolean value that must be set to <cite>true</cite>
if you want to delete a <cite>google_project_iam_policy</cite> that is authoritative.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMPolicy.etag">
<code class="descname">etag</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMPolicy.etag" title="Permalink to this definition">¶</a></dt>
<dd><p>(Computed) The etag of the project’s IAM policy.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMPolicy.policy_data">
<code class="descname">policy_data</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMPolicy.policy_data" title="Permalink to this definition">¶</a></dt>
<dd><p>The <cite>google_iam_policy</cite> data source that represents
the IAM policy that will be applied to the project. The policy will be
merged with any existing policy applied to the project.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMPolicy.project">
<code class="descname">project</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMPolicy.project" title="Permalink to this definition">¶</a></dt>
<dd><p>The project ID. If not specified, uses the
ID of the project configured with the provider.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.IAMPolicy.restore_policy">
<code class="descname">restore_policy</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.IAMPolicy.restore_policy" title="Permalink to this definition">¶</a></dt>
<dd><p>(DEPRECATED) (Computed, only for <cite>google_project_iam_policy</cite>)
The IAM policy that will be restored when a
non-authoritative policy resource is deleted.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.IAMPolicy.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMPolicy.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.IAMPolicy.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.IAMPolicy.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_gcp.projects.OrganizationPolicy">
<em class="property">class </em><code class="descclassname">pulumi_gcp.projects.</code><code class="descname">OrganizationPolicy</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>boolean_policy=None</em>, <em>constraint=None</em>, <em>list_policy=None</em>, <em>project=None</em>, <em>restore_policy=None</em>, <em>version=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy" title="Permalink to this definition">¶</a></dt>
<dd><p>Allows management of Organization policies for a Google Project. For more information see
[the official
documentation](<a class="reference external" href="https://cloud.google.com/resource-manager/docs/organization-policy/overview">https://cloud.google.com/resource-manager/docs/organization-policy/overview</a>) and
[API](<a class="reference external" href="https://cloud.google.com/resource-manager/reference/rest/v1/projects/setOrgPolicy">https://cloud.google.com/resource-manager/reference/rest/v1/projects/setOrgPolicy</a>).</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
<li><strong>boolean_policy</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A boolean policy is a constraint that is either enforced or not. Structure is documented below.</li>
<li><strong>constraint</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Constraint the Policy is configuring, for example, <cite>serviceuser.services</cite>. Check out the [complete list of available constraints](<a class="reference external" href="https://cloud.google.com/resource-manager/docs/organization-policy/understanding-constraints#available_constraints">https://cloud.google.com/resource-manager/docs/organization-policy/understanding-constraints#available_constraints</a>).</li>
<li><strong>list_policy</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A policy that can define specific values that are allowed or denied for the given constraint. It can also be used to allow or deny all values. Structure is documented below.</li>
<li><strong>project</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The project id of the project to set the policy for.</li>
<li><strong>restore_policy</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A restore policy is a constraint to restore the default policy. Structure is documented below.</li>
<li><strong>version</strong> (<em>pulumi.Input</em><em>[</em><em>int</em><em>]</em>) – Version of the Policy. Default version is 0.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_gcp.projects.OrganizationPolicy.boolean_policy">
<code class="descname">boolean_policy</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.boolean_policy" title="Permalink to this definition">¶</a></dt>
<dd><p>A boolean policy is a constraint that is either enforced or not. Structure is documented below.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.OrganizationPolicy.constraint">
<code class="descname">constraint</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.constraint" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the Constraint the Policy is configuring, for example, <cite>serviceuser.services</cite>. Check out the [complete list of available constraints](<a class="reference external" href="https://cloud.google.com/resource-manager/docs/organization-policy/understanding-constraints#available_constraints">https://cloud.google.com/resource-manager/docs/organization-policy/understanding-constraints#available_constraints</a>).</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.OrganizationPolicy.etag">
<code class="descname">etag</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.etag" title="Permalink to this definition">¶</a></dt>
<dd><p>(Computed) The etag of the organization policy. <cite>etag</cite> is used for optimistic concurrency control as a way to help prevent simultaneous updates of a policy from overwriting each other.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.OrganizationPolicy.list_policy">
<code class="descname">list_policy</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.list_policy" title="Permalink to this definition">¶</a></dt>
<dd><p>A policy that can define specific values that are allowed or denied for the given constraint. It can also be used to allow or deny all values. Structure is documented below.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.OrganizationPolicy.project">
<code class="descname">project</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.project" title="Permalink to this definition">¶</a></dt>
<dd><p>The project id of the project to set the policy for.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.OrganizationPolicy.restore_policy">
<code class="descname">restore_policy</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.restore_policy" title="Permalink to this definition">¶</a></dt>
<dd><p>A restore policy is a constraint to restore the default policy. Structure is documented below.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.OrganizationPolicy.update_time">
<code class="descname">update_time</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.update_time" title="Permalink to this definition">¶</a></dt>
<dd><p>(Computed) The timestamp in RFC3339 UTC “Zulu” format, accurate to nanoseconds, representing when the variable was last updated. Example: “2016-10-09T12:33:37.578138407Z”.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.OrganizationPolicy.version">
<code class="descname">version</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.version" title="Permalink to this definition">¶</a></dt>
<dd><p>Version of the Policy. Default version is 0.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.OrganizationPolicy.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.OrganizationPolicy.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.OrganizationPolicy.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_gcp.projects.Service">
<em class="property">class </em><code class="descclassname">pulumi_gcp.projects.</code><code class="descname">Service</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>disable_on_destroy=None</em>, <em>project=None</em>, <em>service=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.Service" title="Permalink to this definition">¶</a></dt>
<dd><p>Allows management of a single API service for an existing Google Cloud Platform project.</p>
<p>For a list of services available, visit the
[API library page](<a class="reference external" href="https://console.cloud.google.com/apis/library">https://console.cloud.google.com/apis/library</a>) or run <cite>gcloud services list</cite>.</p>
<dl class="docutils">
<dt>&gt; <strong>Note:</strong> This resource _must <a href="#id1"><span class="problematic" id="id2">not_</span></a> be used in conjunction with</dt>
<dd><cite>google_project_services</cite> or they will fight over which services should be enabled.</dd>
</dl>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
<li><strong>disable_on_destroy</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – If true, disable the service when the terraform resource is destroyed.  Defaults to true.  May be useful in the event that a project is long-lived but the infrastructure running in that project changes frequently.</li>
<li><strong>project</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The project ID. If not provided, the provider project is used.</li>
<li><strong>service</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The service to enable.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_gcp.projects.Service.disable_on_destroy">
<code class="descname">disable_on_destroy</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.Service.disable_on_destroy" title="Permalink to this definition">¶</a></dt>
<dd><p>If true, disable the service when the terraform resource is destroyed.  Defaults to true.  May be useful in the event that a project is long-lived but the infrastructure running in that project changes frequently.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.Service.project">
<code class="descname">project</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.Service.project" title="Permalink to this definition">¶</a></dt>
<dd><p>The project ID. If not provided, the provider project is used.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.Service.service">
<code class="descname">service</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.Service.service" title="Permalink to this definition">¶</a></dt>
<dd><p>The service to enable.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.Service.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.Service.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.Service.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.Service.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_gcp.projects.Services">
<em class="property">class </em><code class="descclassname">pulumi_gcp.projects.</code><code class="descname">Services</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>disable_on_destroy=None</em>, <em>project=None</em>, <em>services=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.Services" title="Permalink to this definition">¶</a></dt>
<dd><p>Allows management of enabled API services for an existing Google Cloud
Platform project. Services in an existing project that are not defined
in the config will be removed.</p>
<p>For a list of services available, visit the
[API library page](<a class="reference external" href="https://console.cloud.google.com/apis/library">https://console.cloud.google.com/apis/library</a>) or run <cite>gcloud services list</cite>.</p>
<dl class="docutils">
<dt>&gt; <strong>Note:</strong> This resource attempts to be the authoritative source on <em>all</em> enabled APIs, which often</dt>
<dd>leads to conflicts when certain actions enable other APIs. If you do not need to ensure that
<em>exclusively</em> a particular set of APIs are enabled, you should most likely use the
google_project_service resource, one resource per API.</dd>
</dl>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<p>:param pulumi.Input[bool] disable_on_destroy
:param pulumi.Input[str] project: The project ID.</p>
<blockquote>
<div>Changing this forces Terraform to attempt to disable all previously managed
API services in the previous project.</div></blockquote>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><strong>services</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – The list of services that are enabled. Supports
update.</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_gcp.projects.Services.project">
<code class="descname">project</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.Services.project" title="Permalink to this definition">¶</a></dt>
<dd><p>The project ID.
Changing this forces Terraform to attempt to disable all previously managed
API services in the previous project.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_gcp.projects.Services.services">
<code class="descname">services</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_gcp.projects.Services.services" title="Permalink to this definition">¶</a></dt>
<dd><p>The list of services that are enabled. Supports
update.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.Services.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.Services.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.Services.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.Services.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_gcp.projects.UsageExportBucket">
<em class="property">class </em><code class="descclassname">pulumi_gcp.projects.</code><code class="descname">UsageExportBucket</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>bucket_name=None</em>, <em>prefix=None</em>, <em>project=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.UsageExportBucket" title="Permalink to this definition">¶</a></dt>
<dd><p>Allows creation and management of a Google Cloud Platform project.</p>
<p>Projects created with this resource must be associated with an Organization.
See the [Organization documentation](<a class="reference external" href="https://cloud.google.com/resource-manager/docs/quickstarts">https://cloud.google.com/resource-manager/docs/quickstarts</a>) for more details.</p>
<p>The service account used to run Terraform when creating a <cite>google_project</cite>
resource must have <cite>roles/resourcemanager.projectCreator</cite>. See the
[Access Control for Organizations Using IAM](<a class="reference external" href="https://cloud.google.com/resource-manager/docs/access-control-org">https://cloud.google.com/resource-manager/docs/access-control-org</a>)
doc for more information.</p>
<p>Note that prior to 0.8.5, <cite>google_project</cite> functioned like a data source,
meaning any project referenced by it had to be created and managed outside
Terraform. As of 0.8.5, <cite>google_project</cite> functions like any other Terraform
resource, with Terraform creating and managing the project. To replicate the old
behavior, either:</p>
<ul class="simple">
<li>Use the project ID directly in whatever is referencing the project, using the
[google_project_iam_policy](<a class="reference external" href="https://www.terraform.io/docs/providers/google/r/google_project_iam.html">https://www.terraform.io/docs/providers/google/r/google_project_iam.html</a>)
to replace the old <cite>policy_data</cite> property.</li>
<li>Use the [import](<a class="reference external" href="https://www.terraform.io/docs/import/usage.html">https://www.terraform.io/docs/import/usage.html</a>) functionality
to import your pre-existing project into Terraform, where it can be referenced and
used just like always, keeping in mind that Terraform will attempt to undo any changes
made outside Terraform.</li>
</ul>
<p>&gt; It’s important to note that any project resources that were added to your Terraform config
prior to 0.8.5 will continue to function as they always have, and will not be managed by
Terraform. Only newly added projects are affected.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<p>:param pulumi.Input[str] bucket_name
:param pulumi.Input[str] prefix
:param pulumi.Input[str] project</p>
<dl class="method">
<dt id="pulumi_gcp.projects.UsageExportBucket.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.UsageExportBucket.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_gcp.projects.UsageExportBucket.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_gcp.projects.UsageExportBucket.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

</div>
