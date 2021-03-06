## pulumi stack

Manage stacks

### Synopsis


Manage stacks

An stack is a named update target, and a single project may have many of them.
Each stack has a configuration and update history associated with it, stored in
the workspace, in addition to a full checkpoint of the last known good update.


```
pulumi stack [flags]
```

### Options

```
  -h, --help           help for stack
  -i, --show-ids       Display each resource's provider-assigned unique ID
  -u, --show-urns      Display each resource's Pulumi-assigned globally unique URN
  -s, --stack string   The name of the stack to operate on. Defaults to the current stack
```

### Options inherited from parent commands

```
      --color string                 Colorize output. Choices are: always, never, raw, auto (default "auto")
  -C, --cwd string                   Run pulumi as if it had been started in another directory
      --disable-integrity-checking   Disable integrity checking of checkpoint files
  -e, --emoji                        Enable emojis in the output
      --logflow                      Flow log settings to child processes (like plugins)
      --logtostderr                  Log to stderr instead of to files
      --non-interactive              Disable interactive mode for all commands
      --profiling string             Emit CPU and memory profiles and an execution trace to '[filename].[pid].{cpu,mem,trace}', respectively
      --tracing string               Emit tracing to a Zipkin-compatible tracing endpoint
  -v, --verbose int                  Enable verbose logging (e.g., v=3); anything >3 is very verbose
```

### SEE ALSO
* [pulumi](pulumi.md)	 - Pulumi command line
* [pulumi stack export](pulumi_stack_export.md)	 - Export a stack's deployment to standard out
* [pulumi stack graph](pulumi_stack_graph.md)	 - Export a stack's dependency graph to a file
* [pulumi stack import](pulumi_stack_import.md)	 - Import a deployment from standard in into an existing stack
* [pulumi stack init](pulumi_stack_init.md)	 - Create an empty stack with the given name, ready for updates
* [pulumi stack ls](pulumi_stack_ls.md)	 - List all known stacks
* [pulumi stack output](pulumi_stack_output.md)	 - Show a stack's output properties
* [pulumi stack rm](pulumi_stack_rm.md)	 - Remove a stack and its configuration
* [pulumi stack select](pulumi_stack_select.md)	 - Switch the current workspace to the given stack
* [pulumi stack tag](pulumi_stack_tag.md)	 - Manage stack tags

###### Auto generated by spf13/cobra on 16-Jan-2019
