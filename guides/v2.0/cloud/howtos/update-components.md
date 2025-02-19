---
layout: default
group: cloud
subgroup: 10_howto
title: Update components
menu_title: Update components
menu_order: 5
level3_menu_node: level3child
level3_subgroup: upgrade-update
menu_node: 
version: 2.0
github_link: cloud/howtos/update-components.md
---

## How update components {#cloud-howto-upcomp}
This topic discusses how to update components you previously installed from Magento Marketplace or from another source.

Before you continue, you must:

*	Know the component's [Composer name](#update-composer-name) and version
*	Know the component is compatible with your project (in particular, check the required PHP version)

### Find a component's Composer name {#update-composer-name}

{% collapsible Click to expand/collapse content %}

{% include cloud/composer-name.md %}

{% endcollapsible %}

### Get started

{% collapsible Click to expand/collapse content %}

To get started:

{% include cloud/cli-get-started.md %}

{% endcollapsible %}

### Update components

{% collapsible Click to expand/collapse content %}

To update components:

1.	If you haven't done so already, change to your environment root directory.
2.	Make a backup of `composer.json`:

		cp composer.json composer.json.orig
3.	Open `composer.json` in a text editor.
4.	Locate your component.
5.	Update its version.
6.	Save your changes to `composer.json` and exit the text editor.
7.	Update project dependencies:

		composer update
8.	Enter the following commands in the order shown to commit the changes and deploy the project:

		git add -A
		git commit -m "<message>"
		git push origin <environment ID>
9.	Wait for the project to deploy.

	If there are errors, see [Component deployment failure]({{page.baseurl}}cloud/trouble/trouble_comp-deploy-fail.html).

{% endcollapsible %}

#### Related topic
*	[Install components]({{page.baseurl}}cloud/howtos/install-components.html)
*	[Upgrade the Magento system software]({{page.baseurl}}cloud/howtos/upgrade-magento.html)
*	[Install optional sample data]({{page.baseurl}}cloud/howtos/sample-data.html)
*	[Merge and delete an environment]({{page.baseurl}}cloud/howtos/environment-tutorial-env-merge.html)
