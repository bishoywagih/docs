<div class="section" id="module-pulumi_aws.kms">
<span id="kms"></span><h1>kms<a class="headerlink" href="#module-pulumi_aws.kms" title="Permalink to this headline">¶</a></h1>
<dl class="class">
<dt id="pulumi_aws.kms.Alias">
<em class="property">class </em><code class="descclassname">pulumi_aws.kms.</code><code class="descname">Alias</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>name=None</em>, <em>name_prefix=None</em>, <em>target_key_id=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.Alias" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an alias for a KMS customer master key. AWS Console enforces 1-to-1 mapping between aliases &amp; keys,
but API (hence Terraform too) allows you to create as many aliases as
the [account limits](<a class="reference external" href="http://docs.aws.amazon.com/kms/latest/developerguide/limits.html">http://docs.aws.amazon.com/kms/latest/developerguide/limits.html</a>) allow you.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
<li><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The display name of the alias. The name must start with the word “alias” followed by a forward slash (alias/)</li>
<li><strong>name_prefix</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Creates an unique alias beginning with the specified prefix.
The name must start with the word “alias” followed by a forward slash (alias/).  Conflicts with <cite>name</cite>.</li>
<li><strong>target_key_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Identifier for the key for which the alias is for, can be either an ARN or key_id.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_aws.kms.Alias.arn">
<code class="descname">arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Alias.arn" title="Permalink to this definition">¶</a></dt>
<dd><p>The Amazon Resource Name (ARN) of the key alias.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Alias.name">
<code class="descname">name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Alias.name" title="Permalink to this definition">¶</a></dt>
<dd><p>The display name of the alias. The name must start with the word “alias” followed by a forward slash (alias/)</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Alias.name_prefix">
<code class="descname">name_prefix</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Alias.name_prefix" title="Permalink to this definition">¶</a></dt>
<dd><p>Creates an unique alias beginning with the specified prefix.
The name must start with the word “alias” followed by a forward slash (alias/).  Conflicts with <cite>name</cite>.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Alias.target_key_arn">
<code class="descname">target_key_arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Alias.target_key_arn" title="Permalink to this definition">¶</a></dt>
<dd><p>The Amazon Resource Name (ARN) of the target key identifier.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Alias.target_key_id">
<code class="descname">target_key_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Alias.target_key_id" title="Permalink to this definition">¶</a></dt>
<dd><p>Identifier for the key for which the alias is for, can be either an ARN or key_id.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.kms.Alias.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.Alias.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.kms.Alias.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.Alias.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.kms.GetAliasResult">
<em class="property">class </em><code class="descclassname">pulumi_aws.kms.</code><code class="descname">GetAliasResult</code><span class="sig-paren">(</span><em>arn=None</em>, <em>target_key_arn=None</em>, <em>target_key_id=None</em>, <em>id=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.GetAliasResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getAlias.</p>
<dl class="attribute">
<dt id="pulumi_aws.kms.GetAliasResult.arn">
<code class="descname">arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetAliasResult.arn" title="Permalink to this definition">¶</a></dt>
<dd><p>The Amazon Resource Name(ARN) of the key alias.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.GetAliasResult.target_key_arn">
<code class="descname">target_key_arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetAliasResult.target_key_arn" title="Permalink to this definition">¶</a></dt>
<dd><p>ARN pointed to by the alias.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.GetAliasResult.target_key_id">
<code class="descname">target_key_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetAliasResult.target_key_id" title="Permalink to this definition">¶</a></dt>
<dd><p>Key identifier pointed to by the alias.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.GetAliasResult.id">
<code class="descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetAliasResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>id is the provider-assigned unique ID for this managed resource.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.kms.GetCipherTextResult">
<em class="property">class </em><code class="descclassname">pulumi_aws.kms.</code><code class="descname">GetCipherTextResult</code><span class="sig-paren">(</span><em>ciphertext_blob=None</em>, <em>id=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.GetCipherTextResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getCipherText.</p>
<dl class="attribute">
<dt id="pulumi_aws.kms.GetCipherTextResult.ciphertext_blob">
<code class="descname">ciphertext_blob</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetCipherTextResult.ciphertext_blob" title="Permalink to this definition">¶</a></dt>
<dd><p>Base64 encoded ciphertext</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.GetCipherTextResult.id">
<code class="descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetCipherTextResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>id is the provider-assigned unique ID for this managed resource.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.kms.GetKeyResult">
<em class="property">class </em><code class="descclassname">pulumi_aws.kms.</code><code class="descname">GetKeyResult</code><span class="sig-paren">(</span><em>arn=None</em>, <em>aws_account_id=None</em>, <em>creation_date=None</em>, <em>deletion_date=None</em>, <em>description=None</em>, <em>enabled=None</em>, <em>expiration_model=None</em>, <em>key_manager=None</em>, <em>key_state=None</em>, <em>key_usage=None</em>, <em>origin=None</em>, <em>valid_to=None</em>, <em>id=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.GetKeyResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getKey.</p>
<dl class="attribute">
<dt id="pulumi_aws.kms.GetKeyResult.id">
<code class="descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetKeyResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>id is the provider-assigned unique ID for this managed resource.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.kms.GetSecretResult">
<em class="property">class </em><code class="descclassname">pulumi_aws.kms.</code><code class="descname">GetSecretResult</code><span class="sig-paren">(</span><em>id=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.GetSecretResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getSecret.</p>
<dl class="attribute">
<dt id="pulumi_aws.kms.GetSecretResult.id">
<code class="descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetSecretResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>id is the provider-assigned unique ID for this managed resource.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.kms.GetSecretsResult">
<em class="property">class </em><code class="descclassname">pulumi_aws.kms.</code><code class="descname">GetSecretsResult</code><span class="sig-paren">(</span><em>plaintext=None</em>, <em>id=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.GetSecretsResult" title="Permalink to this definition">¶</a></dt>
<dd><p>A collection of values returned by getSecrets.</p>
<dl class="attribute">
<dt id="pulumi_aws.kms.GetSecretsResult.plaintext">
<code class="descname">plaintext</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetSecretsResult.plaintext" title="Permalink to this definition">¶</a></dt>
<dd><p>Map containing each <cite>secret</cite> <cite>name</cite> as the key with its decrypted plaintext value</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.GetSecretsResult.id">
<code class="descname">id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.GetSecretsResult.id" title="Permalink to this definition">¶</a></dt>
<dd><p>id is the provider-assigned unique ID for this managed resource.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.kms.Grant">
<em class="property">class </em><code class="descclassname">pulumi_aws.kms.</code><code class="descname">Grant</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>constraints=None</em>, <em>grant_creation_tokens=None</em>, <em>grantee_principal=None</em>, <em>key_id=None</em>, <em>name=None</em>, <em>operations=None</em>, <em>retire_on_delete=None</em>, <em>retiring_principal=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.Grant" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides a resource-based access control mechanism for a KMS customer master key.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
<li><strong>constraints</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A structure that you can use to allow certain operations in the grant only when the desired encryption context is present. For more information about encryption context, see [Encryption Context](<a class="reference external" href="http://docs.aws.amazon.com/kms/latest/developerguide/encryption-context.html">http://docs.aws.amazon.com/kms/latest/developerguide/encryption-context.html</a>).</li>
<li><strong>grant_creation_tokens</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of grant tokens to be used when creating the grant. See [Grant Tokens](<a class="reference external" href="http://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#grant_token">http://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#grant_token</a>) for more information about grant tokens.
* <cite>retire_on_delete</cite> -(Defaults to false, Forces new resources) If set to false (the default) the grants will be revoked upon deletion, and if set to true the grants will try to be retired upon deletion. Note that retiring grants requires special permissions, hence why we default to revoking grants.
See [RetireGrant](<a class="reference external" href="https://docs.aws.amazon.com/kms/latest/APIReference/API_RetireGrant.html">https://docs.aws.amazon.com/kms/latest/APIReference/API_RetireGrant.html</a>) for more information.</li>
<li><strong>grantee_principal</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The principal that is given permission to perform the operations that the grant permits in ARN format. Note that due to eventual consistency issues around IAM principals, terraform’s state may not always be refreshed to reflect what is true in AWS.</li>
<li><strong>key_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The unique identifier for the customer master key (CMK) that the grant applies to. Specify the key ID or the Amazon Resource Name (ARN) of the CMK. To specify a CMK in a different AWS account, you must use the key ARN.</li>
<li><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – A friendly name for identifying the grant.</li>
<li><strong>operations</strong> (<em>pulumi.Input</em><em>[</em><em>list</em><em>]</em>) – A list of operations that the grant permits. The permitted values are: <cite>Decrypt, Encrypt, GenerateDataKey, GenerateDataKeyWithoutPlaintext, ReEncryptFrom, ReEncryptTo, CreateGrant, RetireGrant, DescribeKey</cite></li>
</ul>
</td>
</tr>
</tbody>
</table>
<p>:param pulumi.Input[bool] retire_on_delete
:param pulumi.Input[str] retiring_principal</p>
<dl class="attribute">
<dt id="pulumi_aws.kms.Grant.constraints">
<code class="descname">constraints</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Grant.constraints" title="Permalink to this definition">¶</a></dt>
<dd><p>A structure that you can use to allow certain operations in the grant only when the desired encryption context is present. For more information about encryption context, see [Encryption Context](<a class="reference external" href="http://docs.aws.amazon.com/kms/latest/developerguide/encryption-context.html">http://docs.aws.amazon.com/kms/latest/developerguide/encryption-context.html</a>).</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Grant.grant_creation_tokens">
<code class="descname">grant_creation_tokens</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Grant.grant_creation_tokens" title="Permalink to this definition">¶</a></dt>
<dd><p>A list of grant tokens to be used when creating the grant. See [Grant Tokens](<a class="reference external" href="http://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#grant_token">http://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#grant_token</a>) for more information about grant tokens.
* <cite>retire_on_delete</cite> -(Defaults to false, Forces new resources) If set to false (the default) the grants will be revoked upon deletion, and if set to true the grants will try to be retired upon deletion. Note that retiring grants requires special permissions, hence why we default to revoking grants.
See [RetireGrant](<a class="reference external" href="https://docs.aws.amazon.com/kms/latest/APIReference/API_RetireGrant.html">https://docs.aws.amazon.com/kms/latest/APIReference/API_RetireGrant.html</a>) for more information.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Grant.grant_id">
<code class="descname">grant_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Grant.grant_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The unique identifier for the grant.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Grant.grant_token">
<code class="descname">grant_token</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Grant.grant_token" title="Permalink to this definition">¶</a></dt>
<dd><p>The grant token for the created grant. For more information, see [Grant Tokens](<a class="reference external" href="http://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#grant_token">http://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#grant_token</a>).</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Grant.grantee_principal">
<code class="descname">grantee_principal</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Grant.grantee_principal" title="Permalink to this definition">¶</a></dt>
<dd><p>The principal that is given permission to perform the operations that the grant permits in ARN format. Note that due to eventual consistency issues around IAM principals, terraform’s state may not always be refreshed to reflect what is true in AWS.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Grant.key_id">
<code class="descname">key_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Grant.key_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The unique identifier for the customer master key (CMK) that the grant applies to. Specify the key ID or the Amazon Resource Name (ARN) of the CMK. To specify a CMK in a different AWS account, you must use the key ARN.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Grant.name">
<code class="descname">name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Grant.name" title="Permalink to this definition">¶</a></dt>
<dd><p>A friendly name for identifying the grant.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Grant.operations">
<code class="descname">operations</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Grant.operations" title="Permalink to this definition">¶</a></dt>
<dd><p>A list of operations that the grant permits. The permitted values are: <cite>Decrypt, Encrypt, GenerateDataKey, GenerateDataKeyWithoutPlaintext, ReEncryptFrom, ReEncryptTo, CreateGrant, RetireGrant, DescribeKey</cite></p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.kms.Grant.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.Grant.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.kms.Grant.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.Grant.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_aws.kms.Key">
<em class="property">class </em><code class="descclassname">pulumi_aws.kms.</code><code class="descname">Key</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>deletion_window_in_days=None</em>, <em>description=None</em>, <em>enable_key_rotation=None</em>, <em>is_enabled=None</em>, <em>key_usage=None</em>, <em>policy=None</em>, <em>tags=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.Key" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides a KMS customer master key.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
<li><strong>deletion_window_in_days</strong> (<em>pulumi.Input</em><em>[</em><em>int</em><em>]</em>) – Duration in days after which the key is deleted
after destruction of the resource, must be between 7 and 30 days. Defaults to 30 days.</li>
<li><strong>description</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The description of the key as viewed in AWS console.</li>
<li><strong>enable_key_rotation</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Specifies whether [key rotation](<a class="reference external" href="http://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html">http://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html</a>)
is enabled. Defaults to false.</li>
<li><strong>is_enabled</strong> (<em>pulumi.Input</em><em>[</em><em>bool</em><em>]</em>) – Specifies whether the key is enabled. Defaults to true.</li>
<li><strong>key_usage</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the intended use of the key.
Defaults to ENCRYPT_DECRYPT, and only symmetric encryption and decryption are supported.</li>
<li><strong>policy</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – A valid policy JSON document. For more information about building AWS IAM policy documents with Terraform, see the [AWS IAM Policy Document Guide](<a class="reference external" href="https://www.terraform.io/docs/providers/aws/guides/iam-policy-documents.html">https://www.terraform.io/docs/providers/aws/guides/iam-policy-documents.html</a>).</li>
<li><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the object.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_aws.kms.Key.arn">
<code class="descname">arn</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Key.arn" title="Permalink to this definition">¶</a></dt>
<dd><p>The Amazon Resource Name (ARN) of the key.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Key.deletion_window_in_days">
<code class="descname">deletion_window_in_days</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Key.deletion_window_in_days" title="Permalink to this definition">¶</a></dt>
<dd><p>Duration in days after which the key is deleted
after destruction of the resource, must be between 7 and 30 days. Defaults to 30 days.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Key.description">
<code class="descname">description</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Key.description" title="Permalink to this definition">¶</a></dt>
<dd><p>The description of the key as viewed in AWS console.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Key.enable_key_rotation">
<code class="descname">enable_key_rotation</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Key.enable_key_rotation" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies whether [key rotation](<a class="reference external" href="http://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html">http://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html</a>)
is enabled. Defaults to false.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Key.is_enabled">
<code class="descname">is_enabled</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Key.is_enabled" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies whether the key is enabled. Defaults to true.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Key.key_id">
<code class="descname">key_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Key.key_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The globally unique identifier for the key.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Key.key_usage">
<code class="descname">key_usage</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Key.key_usage" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the intended use of the key.
Defaults to ENCRYPT_DECRYPT, and only symmetric encryption and decryption are supported.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Key.policy">
<code class="descname">policy</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Key.policy" title="Permalink to this definition">¶</a></dt>
<dd><p>A valid policy JSON document. For more information about building AWS IAM policy documents with Terraform, see the [AWS IAM Policy Document Guide](<a class="reference external" href="https://www.terraform.io/docs/providers/aws/guides/iam-policy-documents.html">https://www.terraform.io/docs/providers/aws/guides/iam-policy-documents.html</a>).</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.kms.Key.tags">
<code class="descname">tags</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.kms.Key.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags to assign to the object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.kms.Key.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.Key.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.kms.Key.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.Key.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

<dl class="function">
<dt id="pulumi_aws.kms.get_alias">
<code class="descclassname">pulumi_aws.kms.</code><code class="descname">get_alias</code><span class="sig-paren">(</span><em>name=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.get_alias" title="Permalink to this definition">¶</a></dt>
<dd><p>Use this data source to get the ARN of a KMS key alias.
By using this data source, you can reference key alias
without having to hard code the ARN as input.</p>
</dd></dl>

<dl class="function">
<dt id="pulumi_aws.kms.get_cipher_text">
<code class="descclassname">pulumi_aws.kms.</code><code class="descname">get_cipher_text</code><span class="sig-paren">(</span><em>context=None</em>, <em>key_id=None</em>, <em>plaintext=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.get_cipher_text" title="Permalink to this definition">¶</a></dt>
<dd><p>The KMS ciphertext data source allows you to encrypt plaintext into ciphertext
by using an AWS KMS customer master key.</p>
<p>&gt; <strong>Note:</strong> All arguments including the plaintext be stored in the raw state as plain-text.
[Read more about sensitive data in state](<a class="reference external" href="https://www.terraform.io/docs/state/sensitive-data.html">https://www.terraform.io/docs/state/sensitive-data.html</a>).</p>
</dd></dl>

<dl class="function">
<dt id="pulumi_aws.kms.get_key">
<code class="descclassname">pulumi_aws.kms.</code><code class="descname">get_key</code><span class="sig-paren">(</span><em>grant_tokens=None</em>, <em>key_id=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.get_key" title="Permalink to this definition">¶</a></dt>
<dd><p>Use this data source to get detailed information about 
the specified KMS Key with flexible key id input. 
This can be useful to reference key alias 
without having to hard code the ARN as input.</p>
</dd></dl>

<dl class="function">
<dt id="pulumi_aws.kms.get_secret">
<code class="descclassname">pulumi_aws.kms.</code><code class="descname">get_secret</code><span class="sig-paren">(</span><em>__has_dynamic_attributes=None</em>, <em>secrets=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.get_secret" title="Permalink to this definition">¶</a></dt>
<dd><p>!&gt; <strong>WARNING:</strong> This data source is deprecated and will be removed in the next major version. You can migrate existing configurations to the [<cite>aws_kms_secrets</cite> data source](<a class="reference external" href="https://www.terraform.io/docs/providers/aws/d/kms_secrets.html">https://www.terraform.io/docs/providers/aws/d/kms_secrets.html</a>) following instructions available in the [Version 2 Upgrade Guide](<a class="reference external" href="https://www.terraform.io/docs/providers/aws/guides/version-2-upgrade.html#data-source-aws_kms_secret">https://www.terraform.io/docs/providers/aws/guides/version-2-upgrade.html#data-source-aws_kms_secret</a>).</p>
<p>The KMS secret data source allows you to use data encrypted with the AWS KMS
service within your resource definitions.</p>
<p>&gt; <strong>NOTE</strong>: Using this data provider will allow you to conceal secret data within your
resource definitions but does not take care of protecting that data in the
logging output, plan output or state output.</p>
<p>Please take care to secure your secret data outside of resource definitions.</p>
</dd></dl>

<dl class="function">
<dt id="pulumi_aws.kms.get_secrets">
<code class="descclassname">pulumi_aws.kms.</code><code class="descname">get_secrets</code><span class="sig-paren">(</span><em>secrets=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.kms.get_secrets" title="Permalink to this definition">¶</a></dt>
<dd><p>Decrypt multiple secrets from data encrypted with the AWS KMS service.</p>
<p>&gt; <strong>NOTE</strong>: Using this data provider will allow you to conceal secret data within your resource definitions but does not take care of protecting that data in all Terraform logging and state output. Please take care to secure your secret data beyond just the Terraform configuration.</p>
</dd></dl>

</div>
