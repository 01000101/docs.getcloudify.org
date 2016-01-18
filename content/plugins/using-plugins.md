---
layout: bt_wiki
title: Using Plugins in Your Application
category: Docs
draft: false
weight: 50

---

### Using Plugins

Cloudify allows users to upload and download plugins to and from the manager, and also to delete and list plugins already on the manager. These abilities are exposed by the rest client via the REST API as well as via the CLI. 

For a list of plugin packages you can download, see [LINK TO PLUGINS DOWNLOAD PAGE]()

To upload a plugin to the manager:

{{< gsHighlight  bash  >}}
$ cfy plugins upload -p /path/to/wagon/archive.wgn
...

Validating /path/to/wagon/archive.wgn
Plugin validated successfully
Uploading plugin '/path/to/wagon/archive.wgn' to management server x.x.x.215
Uploaded plugin successfully, plugin's id is: f82610f0-42d6-4ce4-9efa-9ad21e4fd557
...
{{< /gsHighlight >}}

After uploading the relevant plugin, blueprints can make use of it by having the plugin defined in the blueprint.

{{% gsNote title="Note" %}}
Read more about how to define the plugin in the blueprint [here]({{< relref "blueprints/spec-plugins.md" >}}).
{{% /gsNote %}}

{{% gsTip title="Uploading plugins during bootstrap" %}}
Cloudify enables uploading plugins to the Manager during bootstrap. For more on that, please refer to [Plugin Resources]({{< relref "blueprints/spec-upload-resources.md" >}}).
{{% /gsTip %}}

# What's Next

Cloudify's Team provides a set of Official Plugins you can use. You can find further details about them here, under the `plugins` section.

You can also write your own plugin. To see how, read [this]({{< relref "plugins/creating-your-own-plugin.md" >}}).
