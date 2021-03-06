<div class="section" id="module-pulumi_aws.budgets">
<span id="budgets"></span><h1>budgets<a class="headerlink" href="#module-pulumi_aws.budgets" title="Permalink to this headline">¶</a></h1>
<dl class="class">
<dt id="pulumi_aws.budgets.Budget">
<em class="property">class </em><code class="descclassname">pulumi_aws.budgets.</code><code class="descname">Budget</code><span class="sig-paren">(</span><em>__name__</em>, <em>__opts__=None</em>, <em>account_id=None</em>, <em>budget_type=None</em>, <em>cost_filters=None</em>, <em>cost_types=None</em>, <em>limit_amount=None</em>, <em>limit_unit=None</em>, <em>name=None</em>, <em>name_prefix=None</em>, <em>time_period_end=None</em>, <em>time_period_start=None</em>, <em>time_unit=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.budgets.Budget" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides a budgets budget resource. Budgets use the cost visualisation provided by Cost Explorer to show you the status of your budgets, to provide forecasts of your estimated costs, and to track your AWS usage, including your free tier usage.</p>
<table class="docutils field-list" frame="void" rules="none">
<col class="field-name" />
<col class="field-body" />
<tbody valign="top">
<tr class="field-odd field"><th class="field-name">Parameters:</th><td class="field-body"><ul class="first last simple">
<li><strong>__name__</strong> (<em>str</em>) – The name of the resource.</li>
<li><strong>__opts__</strong> (<em>pulumi.ResourceOptions</em>) – Options for the resource.</li>
<li><strong>account_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ID of the target account for budget. Will use current user’s account_id by default if omitted.</li>
<li><strong>budget_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Whether this budget tracks monetary cost or usage.</li>
<li><strong>cost_filters</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – Map of CostFilters key/value pairs to apply to the budget.</li>
<li><strong>cost_types</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – Object containing CostTypes The types of cost included in a budget, such as tax and subscriptions..</li>
<li><strong>limit_amount</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The amount of cost or usage being measured for a budget.</li>
<li><strong>limit_unit</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The unit of measurement used for the budget forecast, actual spend, or budget threshold, such as dollars or GB. See [Spend](<a class="reference external" href="http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/data-type-spend.html">http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/data-type-spend.html</a>) documentation.</li>
<li><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of a budget. Unique within accounts.</li>
<li><strong>name_prefix</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The prefix of the name of a budget. Unique within accounts.</li>
<li><strong>time_period_end</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The end of the time period covered by the budget. There are no restrictions on the end date. Format: <cite>2017-01-01_12:00</cite>.</li>
<li><strong>time_period_start</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The start of the time period covered by the budget. The start date must come before the end date. Format: <cite>2017-01-01_12:00</cite>.</li>
<li><strong>time_unit</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The length of time until a budget resets the actual and forecasted spend. Valid values: <cite>MONTHLY</cite>, <cite>QUARTERLY</cite>, <cite>ANNUALLY</cite>.</li>
</ul>
</td>
</tr>
</tbody>
</table>
<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.account_id">
<code class="descname">account_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.account_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The ID of the target account for budget. Will use current user’s account_id by default if omitted.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.budget_type">
<code class="descname">budget_type</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.budget_type" title="Permalink to this definition">¶</a></dt>
<dd><p>Whether this budget tracks monetary cost or usage.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.cost_filters">
<code class="descname">cost_filters</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.cost_filters" title="Permalink to this definition">¶</a></dt>
<dd><p>Map of CostFilters key/value pairs to apply to the budget.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.cost_types">
<code class="descname">cost_types</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.cost_types" title="Permalink to this definition">¶</a></dt>
<dd><p>Object containing CostTypes The types of cost included in a budget, such as tax and subscriptions..</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.limit_amount">
<code class="descname">limit_amount</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.limit_amount" title="Permalink to this definition">¶</a></dt>
<dd><p>The amount of cost or usage being measured for a budget.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.limit_unit">
<code class="descname">limit_unit</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.limit_unit" title="Permalink to this definition">¶</a></dt>
<dd><p>The unit of measurement used for the budget forecast, actual spend, or budget threshold, such as dollars or GB. See [Spend](<a class="reference external" href="http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/data-type-spend.html">http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/data-type-spend.html</a>) documentation.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.name">
<code class="descname">name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of a budget. Unique within accounts.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.name_prefix">
<code class="descname">name_prefix</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.name_prefix" title="Permalink to this definition">¶</a></dt>
<dd><p>The prefix of the name of a budget. Unique within accounts.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.time_period_end">
<code class="descname">time_period_end</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.time_period_end" title="Permalink to this definition">¶</a></dt>
<dd><p>The end of the time period covered by the budget. There are no restrictions on the end date. Format: <cite>2017-01-01_12:00</cite>.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.time_period_start">
<code class="descname">time_period_start</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.time_period_start" title="Permalink to this definition">¶</a></dt>
<dd><p>The start of the time period covered by the budget. The start date must come before the end date. Format: <cite>2017-01-01_12:00</cite>.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_aws.budgets.Budget.time_unit">
<code class="descname">time_unit</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.budgets.Budget.time_unit" title="Permalink to this definition">¶</a></dt>
<dd><p>The length of time until a budget resets the actual and forecasted spend. Valid values: <cite>MONTHLY</cite>, <cite>QUARTERLY</cite>, <cite>ANNUALLY</cite>.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.budgets.Budget.translate_output_property">
<code class="descname">translate_output_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.budgets.Budget.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_aws.budgets.Budget.translate_input_property">
<code class="descname">translate_input_property</code><span class="sig-paren">(</span><em>prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.budgets.Budget.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
</dd></dl>

</dd></dl>

</div>
